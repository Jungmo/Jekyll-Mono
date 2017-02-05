---
layout: post
title: OOAD
date: 2016-04-21 05:00:00 +0900
categories: OOAD
---

# Definition

* Analysis - an investiigation of the problem and requirements.
* Design - a conceptual solution that fulfills the requirements
* OOA - examines requirements from the persperctive of the classes and objects
* OOD - to further refine and formalize the analysis model
* method - a disciplined process for generating a set of models
* methodology - a collection of methods applied across the sw dev life cycle.
* model - abstract of system
* RUP - a software engineering process.
* Development case - the choice of practices and UP artifacts for a project may be written up in a short docu.
* UML - a language for specifying, visualizeing, constructing and documenting the artifacts of sw systems.
* use case model - set of all written use cases.
* Scenarios - A specific sequence of actions and interactions between actors and the system
* Extensions - other scenario or branches both success and failure from the main success scenario
* special requirements - if a not-nucntional requirement, quality attributes, and constraint relates specifically to a use case, record it with the use case.

# Modeling Language Characteristics

1. Accurate or formal
2. Consistent
3. Easy to communicate
4. Easy to change
5. Understandable

# Development Cycle and UP phases

1. Inception - business case
2. Elaboration - refined vision, iterative implementation of core architecture.
3. Construction - iterative implementation of remaing lower risk and easier elements
4. Transition - beta test

# Artifacts in inception

1. Vision and Business Case
2. Use-case model
3. Suppementary Specification
4. Glossary
5. Risk list
6. prototypes
7. Developments case
8. Phase Plan
9. Iteration plan

# What is use cases
Use cases are text stories of some actor using a system to meet goals.
# Why use cases
easy ways to capture goals and to keep it simple.

# Type of actor
1. primary actor
2. Supporting actor
3. Offstage actor

# Use case formats
1. brief
2. casual
3. fully-dressed

**check**
# Fully-Dressed Format
1. Stakeholders and Interests
2. Preconditions and postconditions
3. Main success scenario
4. Extensions
5. Special Requirements
6. Technology and data variations List

# How to find use cases
1. Choose the system boundary
2. Identify the primary actors
3. Identify the goals of each primary actors
4. Define use cases that satisfy user goals.

# Three methods of relating use cases
* include
* extend
* generalize

# Type of requirements 
1. Functional
2. Usability
3. Reliability
4. Performace
5. Supportability
6. Packaing
7. Legal
8. Implements
9. Interface
10. Operation

# Requirements arfifact
1. Use case - text stories of some actor using system to meet goals.
2. Supplementary Specification
3. Business rule
4. Glossary
5. Vision

# EBP TEST
A task performed by one person, in one place, at one time in response to a business event, which adds mesuarble business value and leaves the data in consistent state.
state.

# BOSS TEST
Use case should be strongly related to achieving results of measurable value.

# Artifacts in Elaboration
1. Domain Model
2. Design Model
3. Software Architecture doc.
4. Data Model
5. Use-Case Storyboards, UI Prototypes
6. Updates to those started in Inception

# Two kinds of modeling
## Static modeling
* Identify classes using object structuring criteria.
* Define the structural relationships among classes.

## Dynamic modeling
* Define the objects that participate in each use case and their interaction using interaction diagrams.

# Criteria for organizing iterations
1. Risk
2. Coverage
3. Criticality

# Domain Models objective
Identify conceptual classes related to the current iteration

# what does a domain model include?
1. Conceptual classes of domain obj.
2. association between conceptual classes
3. attributes of conceptual classes

# How to create a Domain Model
1. Find the conceptual classes
2. Draw them as classes in a UML class diagram
3. Add association and attributes

# Three strategies to identify conceptual classes
1. Reuse or modify existing models
2. Identify noun phrases - Fully dressed uses cases are an excellent source to draw from.
3. Use a conceptual class category list		

# Elaboration Goals
Bulid the core architecture,
resolve the high-risk elements,
define most requirements, and
estimate the overall schedule and resources

# Logical Architecture
Logical architecture is the large-scale organization of the software classes into packages, subsystems, and layers.
There is no decision about how these elements are deployed across different physical platforms.

# Layer Architecture
A layer is a very coarse-grained grouping of classes, packages, or subsystems that has cohesive responsibility for a major aspect of the system.

# Typical Layers
1. Presentation Layer - UI
2. Application Logic layer(Domain layer) - domain concept
3. Technical service layer - Logging

# Include relationship
* include relationship - a relationship from a base use case to an inclusion use case.
* 여러 유즈케이스가 부분적이 행위를 공통적으로 갖는것. 하나의 하위기능을 수행하는 유스케이스로 분리시키고 포함관계로 연결시키는 것이 좋다.

# Extended relationship
* extend relationship - to append to the existing use case without modifying its orginal text.
* 유즈케이스가 수정되어질수 없을때 유즈케이스를 덧붙힐려면 유즈케이스 내에 언제 어떤 조건에서 기본 유즈켕시스의 행위를 확장하는지 기술하여 기본 유즈케이스의 텍스트를 수정하지않고 기능을 확장한다.

# Domain modeling guideline
* Think lika a mapmaker
* Model the real world

# Diagram can be interpreted differently in different model
* conceptual perspective - conceptual class
* spectification perspective - software abstraction
* implementation perspective - sw implementation

# Association
* association - a relationship btw classes that indicates some meaningful connection
	* 어떤 객체들이 하는 일 사이의 관계를 기억할 필요가 있는가?
* naming
	* ClassName - Verb pharse - ClassName
* Notation
	* 읽는 방향 화살표(생략가능)

# Attribute
* a logical data value of an object
* use case 에서 제안되었거나 기억할 필요가 있는 정보.
* 클래스 박스 안에 적음.( - private, + public, [0..1] option)
* 도메인 모델의 속성은 데이터타입인것이 좋다. conceptual class를 속성이 아닌 연관관계로 관련시켜라.

# System sequence diagram
* 시스템 외부의 액터와 소프트웨어 시스템과 어떻게 상호작용하는가를 설명하는 것. 이때 액터는 시스템 이벤트를 생성시키고 이것은 시스템 오퍼레이션을 요청하는 것이다. 이러한 오퍼레이션을 표현하기 위한 표기법으로서 시퀀스 다이어그램이 있다.
* 시스템 시퀀스 다이어그램은 유즈케이스의 특정 시나리오를 바탕으로 외부의 액터가 발생시키는 이벤트, 이벤트의 순서, 시스템 간의 이벤트를 보여주는 그림이다.
* To identify what events are coming to the system
* To investigate and define the system behaviour as a black box.
* Draw an SSD for a main success scenario and frequent or complex alternative scenarios.
* 한개의 유즈케이스에 여러개의 SSD가 있을 수 있다.
* 실선은 액터가 시스템에게 요청(system operation을 요청), 점선은 시스템이 액터에게 응답.(system이 actor에게 보내주는 information, system event)
* 시스템 이벤트마다 한개씩 작성함(operation contact), 동사로 시작하는 이름.

# Operation contract
* To define system operations
* To create contracts for system operations defined in SSDs.
* describe detailed system behaviour in terms of state changes to obj in the Domain model.
* Precondition, Postcondition.

# Definitions in Operation contract
* Operation : name of operation and parameters
* Cross references : use cases this operation can occur within
* Preconditions : noteworthy assumptions about the state of the system or objs in the Domain Model before execution of the operation
* Postconditions : the state of objs in the Domain Model after completion of the operation
* use cases : the main repository of requirements for the project.
* Domain model : a visual representation of conceptual classes or real-world objects in a domain of interest.
* SSD : for one particular scenario of a use case, the events that external actors generate, their order, and inter-system events.
* Contracts : detailed system behaviour in terms of state changes to objects in the Domain model.
* 도메인 모델의 객체에 대한 변화로써 시스템 behavoiour 를 명확히 하는 것. ???
* Do not forget to include all the associations formed.
* elaboration에서 가장 복잡하고 애매한 시스템 오퍼레이션에서만 약정을 사용한다.

# Postcondition
* include instance creation and deletion, attribute modification, association formed and broken.
* past tense
* theatre stage

# Logical Architecture
* 소프트웨어의 클래스들을 패키지, 서브시스템, 계층과 같은 큰 단위로 구성한 것이다.
* Organization of the sw classes into packages, susbsystems, and layer.
* there is no decision about how these elements are deployed across different physical platform.
* software architecture : the primary carrier of system qualities such as performace, modifiability, security..
* sw arch is the set of significant desisions about the organiztion of a sw system.
* pattern - layered architecture같은거.. MVC..

# Layer 
* 클래스 패키지 및 시스템 내에서 중요하게 협동해야하는 서브시스템등을 매우 큰 크기로 묶어 놓은 것.
* 상위 계층이 하위 계층이 제공하는 서비스를 호출하더록 함.
* presentation Layer : information to externel entities, UI
* Application logic layer : sw objs representing domain concepts that fulfill application requirements, Sale
* Technical Service layer : general purpose objects and subsystems that provide suppporting technical services, such as interfacing with a database or error logging
* SOC - separation of concern(서로 구별되는 계층들로 조직화하며 이 계층들은 연관된 책임을 갖는다. 하위는 일반적인 서비스, 상위는 애플리케이션에 종속적인 서비스.)
* 협력과 결합은 위에서 아래 계층으로 이루어지며, 그 반대로 결합하는 경우는 피하는 것이 좋다.

## benefits using layer
* 분리하면 결합도와 의존관계는 감소하고 cohesion이 향상되며 reusability가 상승하고 reability가 상승한다.

# Model-View Separation Principle
* do not connect or couple non-UI objects directly to UI objects
* 도메인 객체는 뷰객체가 아니기 때문에 뷰객체에 대한 직접적인 지식을 가져서는 안된다.
* do not put application logic in the UI objects.

# MVC Model
* model - view - controller model
model - domain layer
view - UI layer
controller - application layer

## motivation for model-view separation
* To support cohesive model definitions that focus on the domain processes
* To allow separate development of the model and user interface layers
* To minimize the impact of requirements changes in the interface layers
* To allow new views to be easily connected to an existing domain layers
* To allow multiple sumultaneous views on the same model object

# UML is a language for
* Specifying
* Constructing
* Visualizing
* Documenting

# Building Blocks of UML
## Treee kinds of building blocks
* Things
* Relationships
* Diagrams
## Things in UML
* Grouping Things - package
* Annotational things - explanatory parts, note
* Behavioural things
* Structural things


# Structural things
## class
* a description of a set of objects that share the same attributes, operations, relationships, sematics.

## Interface
* a collection of operations that spercify a service of a class or component.

## collaboration
* defines an interaction and is a society of rols and other elements that work together to provide some cooperative behaviour.
* 소프트웨어의 모임.

## Use case
* a description of sequences of actions that a system performs that yield observable result of value to a particular actor

## Active class
* a class whose objects own one or more processes or threads and therfore can initiate control activity.

## Components
* a modular part of the system design that hides its implementation behind a set of external interface

## Aritfact - data
* a physical and replaceable part of a system that contains physical information such as source code files, execuatbles, and scripts

## Nodes - computer
* a physical element that exists at runtime and represents a computational resource, generally habing at least some memoty and processing capability.

# Behaviour things
## Interaction
* a behaviour that comprises **a set of messages exchanged among a set of objects**

## state machine
* a behaviour that specifies the **sequences of states an object** or an interaction goes through during its lifetime in response to events.

## Activity
* a behaviour that specifies the **sequence of steps a computational process perform.** A step of an activity is called an action

# for kinds of relationships in UML
* Associtation - structural relationship
* Realization - semantic relationship
* Generalization - specialization relationship
* Dependency - semantic relationship

# Diagrams in UML
* A diagram is the graphical presentation of a set of elements, rendered as a connected graph of vertices and paths
* visualizes a system grom different persperctives

# Includes 13 kinds of diagrams
## static
* class diagram
* object diagram
* component diagram
* composite suructure diagram
* Deployment diagram
* Artifact diagram

## behaviour
* Use case diagram
* Sequence diagram
* Communication diagram
* State diagram
* Activity diagram

# Extensibility mechanisms
* *stereotypes* extends the vocabulary of the UML, ( </,<뭐시기 뭐시기..>>)
* *tagged value* extends the properties og a UML stereotype. stereotypes의 특성을 적는거.. << >> 밑에..
* *constraints* extends the semantics of a UML building block. UML 블록에 대한 룰을 만들거나 수정하는 것.


# Basic STructural Modeling
* Class Diagrams show a set of classes, interfaces, and colllaborations and their relationship.
* Object Diagrams shows a set of objects and their relationships.
* Component Diagram shows a set of components and their relationships.
* Composite Structure Diagram shows the internal structure of a class or collaboration.
* Deployment Diagram show a set of nodes and their relationships..
* Artifact Diagram shows a set of artifacts and their relationships to their artifacts and to the classes that they implement.

# Class Diagram
## Definition
* a description of a set of objects that share the same attributes, operations, relationships, and semantics.
* name, attributes, operations.

## Techniques
* Identify those things that users or implementers use to describe the problem or solution
* For each abstraction, identify a set of responsibilities
* Provide the attributes and operations that are needed to carry out responsibilities

## Modeling Distribution of Responsibilities
* Identify a set of classes that work together closely to carry out some behaviour
* Identify a set of responsibility for each of these classes
* Look at this set of classes as a whole, split classes that have too much responsibility into smaller abstractions, collapse tiny classes that have trivial responsibilities into larger ones
* Reallocate responsibilities so that each abstraction reasonably stands on its own
* responsibility가 너무 많으면 다른 앱스트랙트로 쪼개든지 하라는 거인듯???

## Well structured class
* provides a crisp abstraction of something drawn from the vocabulary of the problem domain.
* embodies a small, well-defined set of responsibilities
* provides a clear separation of the abstraction's specification and its implementation
* understandable and simple, yet extensible and adaptable

# Relationships
* A relationship is a connection among things.
* Three most-important relationships
	* Dependency
	* generalization
	* association
	
## Dependency
* a semantic connection between two elements, one dependent and one independent
* 종속적인 것과 독립적인 것, 두 개의 요소간의 의미적 결합
* independent element will attect the dependent element
### predifined stereotpyes applicable to Dependency
* import, access(packages)
* bind, derive, permit, instanceOf, instantiate, refine (classes, objects)
* extend, include (use cases)

## Generalization
* the taxonomic relationship between a more general elements(superclass/parent) and a more specific element(subclass/child)
* used for between classes, interfaces, packages, and other elements to show inheritance relationship (실선과 화살표로 표시)

### Applied constraints
* complete : all children have been specified in the model and no others are permitted
* **incomplete** : not all children have been specified and additional children are permiited
* **disjoint** : An object instance will belong to only one subclass
* overapping : An object instance may belong to more than one subclass

## Association
* a structural relationship that specifiess that objects of one thing are connected to objects of another
* name, role, multiplicity

## Aggregation
* the "part-whole", "a-part-of", or "has-a" relationship (다이아몬드 화살표)
* a spectial form of association
* a part can be shared by several composites/wholes

## composite aggregation
* a strong form of aggregation
* requires that a part instance be included in at most one composite at a time
* requires that the composite object has sole responsibility for the disposition of its parts.

## Advanced Associations
* N-ary Association 
