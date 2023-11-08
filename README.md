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

                          
