# JavaScript and Object-oriented programming :frog:
How and when to use OOP in JavaScript?

## What? :open_mouth:
Object oriented programming is a paradigm that tries to reflect real-world problems in form of objects that hold **properties** and **methods**. 
The access :lock: to the properties and methods is limited. Properties and methods are valid in the context of an object, that means that they describe
the features and bahaviour of a specific object. Other names for propetry is field, attribute. Methods are also reffered as procedures or functions.

Objects have a notion of selfness, usually noted with keyword `this` or `self`.
Methods are able to access properties via `this` or `self` and modify them.

A template for an object is called a **class**. Classes provide initial state for objects (values for properties and behaviours implemented in methods).
Class works like a cookie-cutter and the result is an instance of a class (object).

Examples are OOP languages are: Java :volcano:, C++, C#, Python :snake:, R, PHP, JavaScript, Ruby :gem:, Perl, Objective-C, Dart, Swift, Scala, Kotlin, Common Lisp, MATLAB, and Smalltalk.

## Why? :smile:
The main tenets of OOP are: **reusability** and **modularity**. OOP stands on 4 pillars, each representing a strength:

1. :pill: **Encapsulation** - Developer decides which parts of a class are hidden from the "outside world" and which are accessible. It is usually implemented with keywords: `public`, `private` and `protected`.
2. :hatched_chick: **Inheritance** Is-a inheritance is building a new class upon a parent class. Child inherits everything that is not marked as private from the parent. Has-a inheritance is having an instance class A as a part of class B.
3. :red_circle: :large_blue_circle: :large_blue_diamond: **Polymorphism** Child objects are able to run code defined in parent classes. Also, child can overload or override a property/method defined in parent.
4. :icecream: **Generics** (**Data abstraction**) To reduce code duplication, behaviours are defined via interfaces and abstract classes which are then base for concrete class implementations.


## Why not? :bangbang:
OOP is not centered around efficiency of computation and algorithms. The overhead of the object creation and inheritance links between classes may negatively impact the performance. Developers often find themselves writing bloated files to solve simple problems. In general, OOP encourages thickly layered programs that destroy transparency.

## Perfect use scenario
Javascript projects are written using a functional, or event-driven design pattern. In which cases would an OOP pattern be a better choice?

For this task, write a few paragraphs describing a project that would benefit greatly from an OOP structure. (This could be any kind of application, running on any type of system). 

### User stories
Describe the application flow from the user's point of view (user stories). What is the application's purpose, and how would people use it? What information would they enter, and what would be received? Try to mention all the "stories" in which the user performs any kind of CRUD operation.

### System blueprint
Next, using pseudocode (or any other notation-technique or diagramming tool you wish), map out what the main objects of the system would look like, how they would be constructed, and how they would relate to each other. 
