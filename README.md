# OOPS-in-Python
- In Python, object-oriented Programming (OOPs) is a programming paradigm that uses objects and classes in programming. It aims to implement real-world entities like inheritance, polymorphisms, encapsulation, etc. in the programming.
- The main concept of OOPs is to bind the data and the functions that work on that together as a single unit so that no other part of the code can access this data.

### Advantage of python being an Object Oriented Programming Language
- Development and maintenance of Python codes is easier than the procedural programming.
- Python can easily solve the real world problems as it does not works on step by step instructions.
- Data in Python codes are secure due to its special feature of data hiding

## Principles in OOPS
- Object
- Class
- Method
- Inheritance
- Polymorphism
- Encapsulation
- Data Abstruction
  
-  ![image](https://github.com/SourabhKumar2633/OOPS-in-Python/assets/146738264/e90d6a9d-b68d-40c8-a701-19408643bec0)

## PYTHON CLASS 
- A collection of Objects is termed as Class in OOPs concept. Every class has its own unique and distinguishable attributes and methods.
- A class contains the blueprints or the prototype from which the objects are being created. It is a logical entity that contains some attributes and methods.
- Classes are created by keyword of class.
- Attributes are the variables that belong to a class.
- Attributes are always public and can be accessed using the dot (.) operator.
   Eg.: Myclass.Myattribute
- Class Definition Syntax: n

                      class Dog:

	  # class attribute
    	attr1 = "mammal"

      # Instance attribute
	    def __init__(self, name):
		  self.name = name

      # Driver code
      # Object instantiation
      Rodger = Dog("Rodger")
      Tommy = Dog("Tommy")

      # Accessing class attributes
      print("Rodger is a {}".format(Rodger.__class__.attr1))
      print("Tommy is also a {}".format(Tommy.__class__.attr1))

      # Accessing instance attributes
      print("My name is {}".format(Rodger.name))
      print("My name is {}".format(Tommy.name))
  - Output
    - My name is Rodger
    - My name is Tommy

## PYTHON OBJECT
- Anything that has state and behavior can be termed as an Object, be it physical or logical. An Object is an entity mentioned in OOPs concept and is frequently found in Python codes.
- An object consists of:
  - *State*: It is represented by the attributes of an object. It also reflects the properties of an object.
  - *Behavior*: It is represented by the methods of an object. It also reflects the response of an object to other objects.
  - *Identity*: It gives a unique name to an object and enables one object to interact with other objects.

## PYTHON INHERITANCE 
- The property of acquiring all the properties and behaviors of the parent object by an object is termed as inheritance in OOPs
- This is a unique feature in object oriented programming languages which facilitates reusability of the code of the parent class by the derived class.


      # Python code to demonstrate how parent constructors
      # are called.

      # parent class
      class Person(object):

	  # __init__ is known as the constructor
	  def __init__(self, name, idnumber):
		self.name = name
		self.idnumber = idnumber

	  def display(self):
		print(self.name)
		print(self.idnumber)
		
	  def details(self):
		print("My name is {}".format(self.name))
		print("IdNumber: {}".format(self.idnumber))
	
      # child class
      class Employee(Person):
	  def __init__(self, name, idnumber, salary, post):
		self.salary = salary
		self.post = post

		# invoking the __init__ of the parent class
		Person.__init__(self, name, idnumber)
		
	  def details(self):
		print("My name is {}".format(self.name))
		print("IdNumber: {}".format(self.idnumber))
		print("Post: {}".format(self.post))


      # creation of an object variable or an instance
      a = Employee('Rahul', 886012, 200000, "Intern")

      # calling a function of the class Person using
      # its instance
      a.display()
      a.details()
  
- Output
    - Rahul
    - 886012
    - My name is Rahul
    - My name is Rahul
    - Post: Intern


## PYTHON POLYMORPHISM
- OOPs is based on the principle of Polymorphism, which means, that one task can be performed in many ways.
- This code demonstrates the concept of inheritance and method overriding in Python classes. It shows how subclasses can override methods defined in their parent class to provide specific behavior while still inheriting other methods from the parent class.

      class Bird:

	  def intro(self):
		print("There are many types of birds.")

	  def flight(self):
		print("Most of the birds can fly but some cannot.")

      class sparrow(Bird):

	  def flight(self):
		print("Sparrows can fly.")

      class ostrich(Bird):

	  def flight(self):
		print("Ostriches cannot fly.")

      obj_bird = Bird()
      obj_spr = sparrow()
      obj_ost = ostrich()

      obj_bird.intro()
      obj_bird.flight()

      obj_spr.intro()
      obj_spr.flight()

      obj_ost.intro()
      obj_ost.flight()
  
- Object
  
      - There are many types of birds.
      - Most of the birds can fly but some cannot.
      - There are many types of birds.
      - Sparrows can fly.
      - There are many types of birds.
      - Ostriches cannot fly.

 
 
