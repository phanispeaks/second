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

## Methods:
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
**Here we are calling the engine method by using the Car() reference.**

**To summarize, the class provides a blueprint of what should be defined but it does not provide any real content. The Car class above defines the engine but it will not state what a specific car’s engine is. It is specified by the object.**

## Objects:
**The object is an instance of the class. Let’s consider the above example of a car. Here Car is our class and toyota is the object of the car. We can create multiple copies of the object. Every object must be defined using the class.**

**The syntax for creating an object is:**

```python
toyota = Car()
```

**Let’s consider our Car example to understand objects a bit better:**

```python
class Car:

    def engine(self):
        print("Engine")

    def wheel(self):
        print("Wheel")

toyota = Car()
```

**The above toyota = Car() is a class object. Class objects support two kinds of operations: attribute references and instantiation.**

**Class instantiation uses function notation. The instantiation operation (“calling” a class object) creates an empty object.**

**Now we can call different methods from our class Car using the object toyota that we have created. let’s call the method engine and wheel.**

**Open your editor and create a file named mycar.py. In that file copy the code below**

```python
class Car:

    def engine(self):
        print("Engine")

    def wheel(self):
        print("Wheel")


toyota = Car()
toyota.engine()
toyota.wheel()
```

**Save the above code. Now let's take a closer look at our program.**

**Here we are creating a toyota object with the help of Car class. The toyota.engine() is a method object. What exactly happens when a method object is called?**

**In the call toyota.engine() doesn't take any argument but if you see the method declaration we can see that it takes a self argument.**

**You may be confused about why it is not throwing an error. Well whenever we use a method object, the call toyota.engine() is converted to Car.engine(toyota). We will understand more about the self in the upcoming section.**

**Run the program using the following command.**
```python
python mycar.py
```
You'll get the following output:
```python
Engine
Wheel
```
## Constructor:
**The __init__ method is the constructor method in Python. The constructor method is used to initialize the data.**

**Go to the Python shell and enter this example:**
```python
>>> class Car():
...     def __init__(self):
...             print("Hello I am the constructor method.")
...
```
**When we will call our class we will get the following output:**
```python
>>> toyota = Car()
Hello I am the constructor method
```

**Note: You will never have to call the init() method – it gets called automatically when you create a class instance.**


## Instance attributes:
**All the classes have objects and all the objects have attributes. Attributes are the properties. We use __init__() method to specify an object’s initial attribute.**

**Let’s consider our car example:**

```python
class Car():
    def __init__(self, model): 
        self.model = model  #instance attribute
```

**In our example, each Car() has a specific model. Thus instance attributes are unique data to each instance.**

## Class attributes:
**We saw that instance attributes are specific to each object but class attributes are the same for all the instances. Let us look at the example of the car with the help of class attributes.**

```python
class Car():

    no_of_wheels = 4 #class attribute
```

**So each car can have different models but all the cars will have only 4 wheels.**

## Self:
**Now let’s understand what self means and how we use it in object-oriented programming. self represents the instance of a class. By using the self keyword we can access the data initialized in the constructor and methods of a class.**

**Let's look at an example of how self can be used. Let’s create a method named brand under our class Car.**

**Inside that __init__ method, we will pass a model by passing our car’s model name when we are instantiating our object. This name can be accessed anywhere in the class, for example self.model in our case.**

**Go to the file named mycar.py and replace old code with this code:**

```python
class Car(): 

  def __init__(self, model): 
    self.model = model
  		
  def brand(self): 
    print("The brand is", self.model)  

car = Car("Bmw")
car.brand()
```

**Now when we run our above program using the following command:**

```python
python mycar.py
```

**We will get the following output:**
```python
The brand is Bmw
```
**Note: self is a convention and not a real Python keyword. self is an argument in a method and we can use another name in place of it. But it is recommended to use self because it increases the readability of  your code.**

## Inheritance:
**Inheritance refers to when a class inherits the property of another class.**

**The class from which properties are inherited is called the base class. The class which inherits the property of another class is called the derived class.**

**Inheritance can be defined as a parent and child relationship. The child inherits the properties of the parent. Thus making the child a derived class while parent is a base class. Here the term property refers to attributes and methods.**

**The syntax for a derived class definition looks like this:**

```python
class DerivedClassName(BaseClassName):
    <statement-1>
    .
    .
    .
    <statement-N>
```
**It’s important to note that child classes override or extend the attributes and behaviors of parent class methods. This is to say that child classes inherit all of the the attributes and behaviors of their parents – but they're also able to specify different behavior to follow.**

**The most basic type of class is an object, which generally all other classes inherit as their parent. Let’s modify our previous example to understand how inheritance works.**

**We will create a base class named vehicle:**

```python
class Vehicle:
    def __init__(self, name):
        self.name = name
    
    def getName(self):
        return self.name
```
**We have created a class Vehicle and instantiated a constructor with self.name which we are using in getName method. Whenever this method will be called, it will return the name that has been passed when an object is instantiated for that class.**

**Now let’s create a child class Car:**

```python
class Vehicle:
    def __init__(self, name):
        self.name = name
    
    def getName(self):
        return self.name

class Car(Vehicle):
  pass
```

**Car is a child class of Vehicle. It inherits all the method and attributes of parent class.**

**Now let’s use methods and attribute from the Vehicle class in our child class Car.**

```python
class Vehicle:

    def __init__(self, name, color='silver'):
        self.name = name
        self.color = color
    
    def get_name(self):
        return self.name
    
    def get_color(self):
        return self.color

class Car(Vehicle):
  pass

audi = Car("Audi r8")
print("The name of our car is", audi.get_name(), "and color is", audi.get_color())
```

**Let's understand what we have done here.**

**We have declared a class named Vehicle with a constructor that takes name as an argument while color has a default argument.**

**We have two methods inside it. get_name returns name while get_color returns the color. We have instantiated an object and passed the car name.**

**One thing you'll notice here that we are using base class methods in our child class declaration.**

**Run the above program using the following command:**
```python
python mycar.py
```
**Output:
```python
The name of our car is Audi r8 and color is silver
```
**We can also override a parent method or attribute. In the above example, we have defined our vehicle color has silver. But what if the color of our car is black?**

**Now for every child class, we can’t make changes in the parent class. There comes the overriding functionality.**
```python
class Vehicle:

    def __init__(self, name, color='silver'):
        self.name = name
        self.color = color
    
    def get_name(self):
        return self.name
    
    def get_color(self):
        return self.color

class Car(Vehicle):

    def get_color(self):
        self.color = 'black'
        return self.color

audi = Car("Audi r8")
print("The name of our car is", audi.get_name(), "and color is", audi.get_color()
```
**As you can see in the above program, I have not instantiated a constructor. The reason behind this is that our child class Car is only using attributes from the Vehicle class and it is already inheriting them. So in such a scenario, there is no need to re-instantiate these attributes.**

**Now when we run the above program we will get the following output:**
```python
The name of our car is Audi r8 and color is black
```

## Super:
**super()  returns a temporary object of the superclass that then allows us to call that superclass’s methods.**

**Calling the previously built methods with super() saves us from needing to rewrite those methods in our subclass, and allows us to swap out superclasses with minimal code changes. Thus super extends the functionality of the inherited method.**

**Let’s extend our car example using super(). We will instantiate a constructor with brand_name and color in the parent class, Vehicle. Now we will call this constructor from our child class (Car) using super. We will create a get_description method which is returning self.model from Car class and self.brand_name, self.color from the Vehicle class.**

```python
class Vehicle:
 
    def __init__(self, brand_name, color):
        self.brand_name = brand_name
        self.color = color
 
    def get_brand_name(self):
        return self.brand_name
 
class Car(Vehicle):
 
    def __init__(self, brand_name, model, color):  
        super().__init__(brand_name, color)       
        self.model = model
 
    def get_description(self):
        return "Car Name: " + self.get_brand_name() + self.model + " Color:" + self.color
 
c = Car("Audi ",  "r8", " Red")
print("Car description:", c.get_description())
print("Brand name:", c.get_brand_name())
```
**When we run the above program we get following output:**
```python
Car description: Car Name: Audi r8 Color: Red
Brand name: Audi
```







