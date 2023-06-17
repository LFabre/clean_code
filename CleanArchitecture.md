# Clean Architecture - Notes

This repository presents all the notes I made while reading the book
Clean Architecture from Robert C. Martin. I've also extracted a few paragraphs
which I found to be important.

## Part I - Introduction

"The word “architecture” is often used in the context of something at a high
level that is divorced from the lower level detail, whereas “design” more often
seems to imply structures and decisions at a lower level. But this usage is
nonsensical when you look at what a real architect does."

"The low-level details and the high-level structure are all part of the same
whole. They form a continuous fabric that defines the shape of the system. You
can't have one without the other; indeed, no clear dividing line separates
them. There is simply a continuum of decisions from the highest to the lowest
levels."

The measure of design quality can be measured by the amount of changes required
to implement new features. When many changes are required the deign is bad.
A good design minimizes effort and maximize productivity. __Focus on building
systems that are easy to change__.

On this chapter the author also makes some references to the book Clean Code.
He remembers the rules of the _The Boy Scout_ and _The only way to go fast is to go well_

## Part II - Starting with the Bricks

### Structured Programming

_Structured programming imposes discipline on direct transfer of control._

Structured programming is a programming paradigm witch enforces the use of
control structures to control the flow of a program. These structures take the
form, on many languages, as statements such as `if`, `do`, `while`, etc.

### Object-Oriented Programming

_Object-Oriented programming imposes discipline on indirect transfer of control._

Object-oriented programming (OOP) is defined as a programming paradigm built on the
concept of objects, which can contain data in the form of attributes and behaviors
in the form of procedures.

Some key components of Object-oriented programming are:

- __Class__: The blueprint of an object. A class defines the structure, components and
the behavior of objects.
- __Object__: The instance of a class.
- __Methods__: -
- __Attributes__: -

Some key concepts of Object-oriented programming are:

- __Encapsulation__: The process of grouping functions and data into a single entity, where only a few set of information is exposed to other entities.
- __Inheritance__: The process of passing properties and behaviors, through declaration,
of an object based to another.
- __Polymorphism__: Allow multiple objects to have the same behaviors but implemented
in different forms.

### Functional Programming

_Functional programming imposes discipline upon assignment._

## Part III - Design Principles

- __S__ ingle Responsibility Principle
  - _A Module should be responsible to one, and only one, actor_
  - _Separate the code that different actors depend on_
- __O__ pen-Closed Principle
  - _A software artifact should be open for extension and closed for modification_
  - This characteristic will preserve the ability of the software to evolve without demanding
  too many changes. This can be achieved by decomposing the system in multiple modules where
  the ones on higher levels are protected from changes in hte ones of lower levels.
- __L__ iskov Substitution Principle
  - An object and a sub-object must be interchangeable without breaking the program.
  - _"Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T."_
- __I__ nterface Segregation Principle
  - Segregate components interaction in a way that only the essential methods are exposed. Do not allow for components to require or depend on methods they don't need.
- __D__ ependency Inversion Principle
  - Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.
