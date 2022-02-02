# Design Patterns

-   Typical solutions to commonly occuring problems in software design
-   pre-made blueprints that you can customize to solve a recurring design problem in your code
-   **NOT A SPECIFIC PIECE OF CODE**
-   Follow the pattern details and implement a solution that suits the realities of your own program.
-   Sections usually present in a pattern description
    -   **Intent**
        -   briefly decribes both the problem and solution
    -   **Motivation**
        -   further explains the problem and the solution the pattern makes possible
    -   **Structure**
        -   shows each part of the pattern and how they are related
    -   **Code Example**
        -   explicit examples in the programming language you're designing make it easier to grasp the pattern

# **Singleton**

-   this is a creational design pattern
-   ensure that a class has only on instance, while providing a global access point to this instance

## Problem

-   Ensure that a class has just a single instance
    -   control access to some shared resource
-   Provide a global access point to that instance
    -   allows you to access some object from anywhere in the program
    -   protects that instance from being overwritten by other code

## Solution

-   Make the default constructor private
    -   this prevents other objects from using the new operator with the Singleton class
-   Create a static creation method that acts as a constructor
    -   under the hood thhis call the private constructor to create an object and saves it in a static field
    -   whenever the method is called, the same object is always returned

## Applicability

-   Use this pattern when a class in your program should have just a single instance available to all clients
    -   single database object shared by different parts of the program
    -   Disables all other means to creating objects of a class except for the special creation method
    -   eithe creates a new object t or returnds an existing one
-   You need stricter control over global variables
    -   Nothing except the Singleton class itself can replace the cached instance

## Advantages

-   Can be sure that class has only a single instance
-   you gain a global access point to that instance
-   signleton object is initialized only when it's requested for the first time

## Disadvantages

-   can mask bad design when components of the program know too much about each other
-   requires special treatment in a multithreaded environment so that multiple threads won't create a singleton object several time
-   difficult to test because many test rely on inheritance when producing mock objects
    -   either don't write the test
    -   or don't use singleton

# **Factory**

-   provides an interface for creating objects in a superclass
-   allows subclasses to alter the type of objects that will be created

## Problem

-   Create your first application to handle everything of one instance (majority of code is handled in one place)
-   What happens if you get asked to develop for additional instances?
-   Most of your code is coupled to that initial instance
    -   If you need to add another you might have to re-create the initial instance and refactor some of it's code, which can be a daunting task
-   Plus what happens if you get asked for even MORE! instances?
    -   this would force you to re-write the code over and over and over again
    -   leads to nasty looking code

## Solution

-   replace direct object construction calls with calls to a special "factory" method
-   Objects are still created with new operator but it's being called from within the factory method
-   Objects returned by a factor method are often referred to as products
-   This allows you to override methods and constructor in a subclass and change what's being created by the method
-   often called client code
    -   clients treat all products as abstract from the factory
    -   they know specific methods that all factory objects are suppose to have, but exactly how it works isn't important to the client

## Applicability

-   When you don't know beforehand the exact types and dependencies of the objects your code should work with
    -   separates the product construction code from the code that actually uses the product
    -   easier to extend the product consturction code independently
-   When you want to provide users of your library or frameowrk with a way to extend its internal components
-   When you want to save system reousrces by re-using existing objects instead of rebuilding them each time

## Advantages

-   Avoid tight coupling between the creator and concrete products
-   Single responsibility princle. can move product creation code into one place in the program
-   Open/Close principle, introducing new types of products into the code without breaking it

## Disadvantages

-   Code may become more compl;icated since you need to introduce a new subclass to implementations for the pattern.

Good Resource for more in-depth nature on design patterns:

[refacotring.guru](https://refactoring.guru/design-patterns)
