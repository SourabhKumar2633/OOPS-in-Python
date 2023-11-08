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

 ## Python Encapsulation
  - OOPs restrict direct access to its methods and variables by encapsulating the code and data together.
  - Encapsulation is one of the fundamental concepts in object-oriented programming (OOP). It describes the idea of wrapping data and the methods that work on data within one unit.
  -  This puts restrictions on accessing variables and methods directly and can prevent the accidental modification of data. To prevent accidental change, an object’s variable can only be changed by an object’s method. Those types of variables are known as private variables.
  -  A class is an example of encapsulation as it encapsulates all the data that is member functions, variables, etc

  - ![image](https://github.com/SourabhKumar2633/OOPS-in-Python/assets/146738264/23adb496-b1bc-4869-aaa4-524c69af6356)

        # Python program to
        # demonstrate private members

        # Creating a Base class
        class Base:
	    def __init__(self):
		self.a = "GeeksforGeeks"
		self.__c = "GeeksforGeeks"

        # Creating a derived class
        class Derived(Base):
	    def __init__(self):

		# Calling constructor of
		# Base class
		Base.__init__(self)
		print("Calling private member of base class: ")
		print(self.__c)


        # Driver code
        obj1 = Base()
        print(obj1.a)

        # Uncommenting print(obj1.c) will
        # raise an AttributeError

        # Uncommenting obj2 = Derived() will
        # also raise an AtrributeError as
        # private member of base class
        # is called inside derived class

 ## DATA ABSTRUCTION
 - It hides unnecessary code details from the user. Also,  when we do not want to give out sensitive parts of our code implementation and this is where data abstraction came.
 - Data Abstraction in Python can be achieved by creating abstract classes.

       class MyClass: 

       # Hidden member of MyClass 
       __hiddenVariable = 0
	
	   # A member method that changes 
	   # __hiddenVariable 
	   def add(self, increment): 
		self.__hiddenVariable += increment 
		print (self.__hiddenVariable) 

       # Driver code 
       myObject = MyClass()	 
       myObject.add(2) 
       myObject.add(5) 

       # This line causes error 
       print (myObject.__hiddenVariable) 
 - Output
   
       2
       7
       Traceback (most recent call last):
       File "filename.py", line 13, in 
       print (myObject.__hiddenVariable)
       AttributeError: MyClass instance has 
       no attribute '__hiddenVariable'

   - We can access the value of a hidden attribute by a tricky syntax:

         # A Python program to demonstrate that hidden 
         # members can be accessed outside a class 
         class MyClass: 

	     # Hidden member of MyClass 
	     __hiddenVariable = 10

         # Driver code 
         myObject = MyClass()	 
         print(myObject._MyClass__hiddenVariable)

     - Output

           10

   
 
 
 
