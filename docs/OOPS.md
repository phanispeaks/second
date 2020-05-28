# OOP concepts:
**Python is a multi-paradigm programming language. It means Python can use different approaches to solve a problem. One of the paradigms is procedural or functional programming. It structures the code like a recipe – a set of steps in the form of functions and code blocks.**

**Another approach to solving the problem is by creating classes and objects. This is known as object-oriented oriented programming. An object is a collection of data (variables) and methods that act on those data. And classes are a blueprint for each object.**

**The important thing to understand in object-oriented programming is that objects are at the center of the paradigm – they not only represent the data but also the structure of the program.**

**You can choose the paradigm that best suits the problem at hand, mix different paradigms in one program, and/or switch from one paradigm to another as your program evolves.**

## Advantages of object oriented programming
**Inheritance: This is one of the most useful concepts in OOP. It specifies that the child object will have all the properties and behavior of the parent object. Thus Inheritance allows us to define a class that inherits all the methods and properties from another class.**
**Polymorphism: To understand polymorphism let’s divide the word into two parts. The first part "poly" means many and "morph" means to form or shape. Thus polymorphism means one task can be performed in many different ways.**

**For example, you have a class animal, and all animals speak. But they speak differently. Here, the “speak” behavior is polymorphic and depends on the animal. So, the abstract “animal” concept does not actually “speak”, but specific animals (like dogs and cats) have a concrete implementation of the action “speak”.**

**Polymorphism means the same function name or method name being used for different types.**
**Encapsulation: In object-oriented programming you can restrict access to methods and variables – we can make the methods and variables private. This can prevent the data from being modified by accident and is known as encapsulation.**
**First, we will understand classes, objects, and constructors. Then after that, we will look into the above properties again. If you already know about classes, objects, and constructors, feel free to skip ahead.**

## Classes:
**There are primitive data structures available in Python, for example, numbers, strings, and lists. These can all be used for simple representations like name, place, cost, and so on.**

**But what if we have more complex data? If there is a pattern in the repetition of the properties of that data, what can we do?**

**Suppose we have 100 different animals. Every animal has a name, age, legs, etc. What if we want to add other properties to each animal, or one more animal gets added to that list? To manage such a complex scenario we need classes.**

**According to the official Python documentation:**

**Classes provide a means of bundling data and functionality together. Creating a new class creates a new type of object, allowing new instances of that type to be made.**
**Each class instance can have attributes attached to it for maintaining its state. Class instances can also have methods (defined by its class) for modifying its state.**

**Syntax of class:**

```python
class ClassName:
    <expression-1>
    .
    .
    .
    <expression-N>
```

**We use class keyword to define a class. We will define a class Car.**

```python
class Car:
    pass
```

### Methods:
**Methods look the same as functions. The only difference is that methods are dependent on an object. A function can be invoked by name while methods need to be invoked by using their class reference. They are defined inside the class.**

**In our example, let's create two methods. One is an engine and another is a wheel. These two methods define the parts available in our car.**

**The below program will give us a better idea of classes:**
```python
>>> class Car:
...     def engine(self):
...             print("Engine")
...

>>> Car().engine()
Engine
```

