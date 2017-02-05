---
layout: post
title: RNN example using tensorflow
data: 2016-07-13
categories: tensorflow
---
# RNN


### Creating RNN Cell
```python
# RNN model
rnn_cell = rnn_cell.BasicRNNCell(rnn_size)
```
rnn_size는 output Layer의 vector 차원? 으로 생각하면 될 듯(예제에선 4)

```python
rnn_cell = rnn_cell.BasicLSTMCell(rnn_size)
rnn_cell = rnn_cell.GRUCell(rnn_size)
```

Basic RNN이 아닌 더 성능 좋은 것을 쓸려면 위와 같은 것을 사용한다.

```python
outputs, state = rnn.rnn(rnn_cell, X_split, state)
```
X_split은 몇 개의 스테이트를 사용할 지 나타낸다

![alt text](https://github.com/Jungmo/jungmo.github.com/blob/master/_posts/img/rnn.png?raw=true "RNN")

* 파라미터 안에 있는 state는 초기 스테이트(처음엔 0으로 지) 하던 것과 이어서 쓰고 싶을때 사용할 수 있다
* 변수 state는 각각 실행때마다 변하는 스테이트
* outputs는 그림에서의 y값.

`type X_split`

shape = (1,4) 1은 batch size 4는 벡터의 차원(예제에선 4 , h,e,l,o)


`type output`

shape = (1,4) 1은 batch size 4는 rnn_size

x_data = np.array([ [1,0,0,0], #h
                    [0,1,0,0], #e
                    [0,0,1,0], #l
                    [0,0,1,0]],#o
                    dtype='f')
                    
### RNN model
```
rnn_cell = rnn_cell.BasicRNNCell(rnn_size)
state = tf.zeros([batch_size, rnn_cell.state_size])
X_split = tf.split(0,time_step_size, x_data)
outputs, state = rnn.rnn(rnn_cell, X_split, state)
```

state는 제일 처음에 0이고 batch_size와 state_size로 텐서의 사이즈를 정함

**time_step_size**는 몇개의 스테이트를 사용하는 지이다.

### Cost

```
logits = tf.reshape(tf.concat(1,outputs), [-1, rnn_size])
targets = tf.reshape(sample[1:], [-1])
weights = tf.ones([time_stop_size * batch_size])

loss = tf.nn.seq2seq.sequence_loss_by_example([logits], [targets], [weights])
cost = tf.reduce_sum(loss) / batch_size
train_op = tf.train.RMSPropOptimizer(0.01, 0.9).minimize(cost)
```

logits은 예측값(y hat), target은 실제값(y), weights는 1로 준다

logits는 2D[batch_size, num_decoder_symbols]

targets는 1D batchsized int32 weight는 1d batchsized double

targets은 예를들어 hello일때 ello에 맞춰줘야한다. 그래서 [1:]로 제일 앞꺼 빼줌

### Train & Prediction

with tf.Session() as sess:
    tf.initialize_all_variables().run()
    for i in range(100):
        sess.run(train_op)
        result = sess.run(tf.arg_max(logits,1))
        print(result, [char_rdic[t] for t in result])
        
logits은 예측값이었다. 

![alt text](https://github.com/Jungmo/jungmo.github.com/blob/master/_posts/img/rnncode.png?raw=true "code")

출처 : [hunkim@github](http://hunkim.github.io/ml/)

