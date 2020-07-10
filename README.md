# JavaScript :watermelon: and Object-oriented programming :frog:
When I think of JavaScript and its applications, OOP is not the first thing that comes into my mind.
JavaScript does not impose an object-oriented paradigm on its own, it's flexible so you can apply the paragidm when you see fit.

In this short overview I'm going to answer the question: How and when to use OOP in JavaScript?

## What? :open_mouth:
Quick brush-up.

Object oriented programming is a paradigm that tries to reflect real-world problems by creating objects holding **properties** and **methods**. 
Properties and methods are valid in the context of an object, that means that they describe
the features and bahaviours of a specific object. In the vast ocean of OOP languages property may be called a field, attribute. Methods are also reffered as procedures or functions. The access :lock: to the properties and methods is limited via keywords: **public**, **protected**, **private**. 

Objects have a notion of selfness, usually noted with keyword `this` or `self`.
Methods are able to access properties via `this` or `self` and modify them. Methods can be invoked the same way. 

A template for an object is called a **class**. Classes provide initial state for objects (default values for properties and behaviours implemented in methods).
Class works like a cookie-cutter and the result is an instance of a class (object).

Examples are OOP languages are: Java :volcano:, C++, C#, Python :snake:, R, PHP, JavaScript, Ruby :gem:, Perl, Objective-C, Dart, Swift, Scala, Kotlin, Common Lisp, MATLAB, and Smalltalk.

## Why? :smile:
The main tenets of OOP are: **reusability** and **modularity** :1+:. OOP stands on 4 pillars:

1. :pill: **Encapsulation** - Developer decides which parts of a class are hidden from the "outside world" and which are accessible. :box: It is usually implemented with keywords: `public`, `private` and `protected`.
2. :hatched_chick: **Inheritance** Is-a inheritance is building a new class upon a parent class. Child inherits everything that is not marked as private from the parent. Has-a inheritance is having an instance class A as a part of class B.
3. :red_circle: :large_blue_circle: :large_blue_diamond: **Polymorphism** Child objects are able to run code defined in parent classes. Also, child can overload or override a property/method defined in parent.
4. :icecream: **Generics** (**Data abstraction**) To reduce code duplication, behaviours are defined via interfaces and abstract classes which are then base for concrete class implementations.

If I had to squeeze the essence of the paradigm into one sentence it would be: OOP closely associates bahaviours with data.

## Why not? :pouting_cat:
But wait! If OOP is generally accepted as the most popular method of programming, doesn't it mean it's the best?
As you may already suspect, one solution doesn't fit all. With all the advantages of OOP, it is far away from perfection.
OOP sets your mindset on a specific track. It will take you places, but not everywhere.

As was already mentioned, OOP is to reflect real world to ease development for human. The abstraction introduced is totally unnecessary for machines themselves. It is for the programmer to enforce rules into projects that oterwise would be hard to keep track of.  
OOP is not centered around efficiency of computation and algorithms. The overhead of the object creation and inheritance links between classes may negatively impact the performance. Developers often find themselves writing bloated files to solve simple problems. In general, OOP encourages thickly layered programs that destroy :boom: transparency.

## Other approaches

### Functional programming
Adhering to functional programming means organizing code into functions and keeping data immutable (data is copied, no modified). This leads to writing programs with no side effects (what happens inside of functional, stays inside the function :sunglasses:). In functional code, a function is not able to change the outside world (the state of the object or system), and the output value is fully deterministic (always the same for the same input) and depends only on the given arguments. System remains **stateless**. This allows to keep strong control over the program flow. Examples of functional programming languages are:  Scala, F#, Wolfram Language, Lisp, Standard ML, DAML and Clojure.

Pros :smiley:
- Avoid statefulness
- Avoid side effect

Use cases :bulb:
- **Industrial apps** :factory:
- **finance apps for risk analytics** :bar_chart: :moneybag: :bank:
- Fault-tolerant :white_check_mark: systems where performance :fast_forward: is the :key:

### Event-driven programming
The flow of the program is determined by events such as user actions (mouse clicks, key presses), sensor outputs, or messages from other programs or threads. Usually, there exists a main loop, a listener :ear:, that triggers callback functions in response to specific events occurring. 

Pros :sunflower:
- Easy way to program interactive apps
- Flexible

Use cases:
- web applications centered around responsing to (user's) actions
- device drivers :rocket:
- GUI-centered apps :fireworks:


## Perfect use scenario
Javascript projects are written using a functional, or event-driven design pattern. In which cases would an OOP pattern be a better choice?

Use OOP when you need to:
- represent real-world notions with classes (employees, animals, species, invoices)
- organize code into units
- present data from database, carry out CRUD* operations on the data, it's usually done [ORM](https://en.wikipedia.org/wiki/Object-relational_mapping) (Object-relational mapper)

* CRUD -  create, read, update, and delete. The :four: basic functions of persistent storage. :gift:


For this task, write a few paragraphs describing a project that would benefit greatly from an OOP structure. (This could be any kind of application, running on any type of system). 
Let's consider a project that would greatly benefit from OOP rather than the other approaches: a multi-player quiz application.
The example game requires 2+ players, set of questions and answers (with only 1 correct one), set of rules and logic that drives the whole quiz, keeps track of the score, determines the winner and losers.

The app would require modeling a number of classes:
- quiz game (quiz's logic, keeping the number of rounds etc.)
- player (with score, name fields and methods for updating score)
- question (question, the correct answer, other incorrect alternatives)

### User stories

1. As a quiz master, I want to load a text file into the program with questions and possible answers. The program loads the data into a collection and marks which answer is correct for any question.
1b. As a quiz master, I want to choose the number of rounds in the game.
2. As a player, I want to input my name and profile photo into the program before the game starts.
3. As a player, I want to have score of 0 at the beginning of the game.
4. As a player, I want to be given 1 question each round.
5. As a quiz master, I want the program to calculate and show the winner table after all rounds are finished.
6. As a player, I want to be able to save my score in my profile.
7. As a player, I choose the correct answer, I want my score to be updated to +1.

A READ operation would be performed for story 1, 4.
An UPDATE operation would be performed for story 7.
A CREATE operation would be performed for story 2, 3, 6.

### System blueprint
The diagram below shows 3 classes: Game, Player, QuestionSet. The relations between them are aggregation.
A game consists in parent-child relation with many Players and QuestionSets.
You can also see fields and methods available in the classes.

![alt text](https://github.com/marta-krzyk-dev/JavaScriptOOP/blob/master/QuizDiagram.png?raw=true)
