# Android-OOP-Interview-Questions-Answer


**1. What is an Object ?**

    An object is an instance of a class that has states and behaviors. A Class can be defined as a template that describes 
    the behavior/state that the object of its type support.
    
**2. What is the main feature of OOP ?**

    Encapsulation, Polymorphism, Inheritance, Abstraction
    
**3. What is encapsulation ?**

    Encapsulation is one of the four fundamental OOP concepts. It is a mechanism of wrapping the data (variables) and code acting 
    on the data (methods) together as a single unit. In encapsulation, the variables of a class will be hidden from other classes, 
    and can be accessed only through the methods of their current class. Therefore, it is also known as data hiding. To achieve encapsulation in Java:

    Declare the variables of a class as private.
    Provide public setter and getter methods to modify and view the variables values.
    Benefits of Encapsulation:

    The fields of a class can be made read-only or write-only.
    A class can have total control over what is stored in its fields.
  
**4. What is Polymorphism ?**

    The word polymorphism means having many forms. In simple words, we can define polymorphism as the ability of a message to be displayed 
    in more than one form. In Java polymorphism is mainly divided into two types: compile-time and runtime polymorphism.
  
**5. What is the difference between static and dynamic Polymorphism ?**
  
    method overloading represents a static form of polymorphism. method overloading means using two or more functions with same name 
    but with the different parameters. Static polymorphism is resolved on compile-time and that is why it's called static.
    
    An example of this would be as follow:

    class StaticPolymorphismTest {
      public int multiply(int a, int b) {
        return a * b;
      }
      public double multiply(double a, double b) {
        return a * b;
      }
    }
    
    method overriding represents a dynamic form of polymorphism. It is a process in which a function call to the overridden method is resolved at Runtime. 
    It is also known as Dynamic Method Dispatch. dynamic polymorphism is resolved at runtime. An example of this would be as follow:

    class Parent {
        void Print()
        {
            System.out.println("parent class");
        }
     }
     
     class subclass1 extends Parent {
        void Print()
        {
            System.out.println("subclass1");
        }
     }
     class subclass2 extends Parent {
        void Print()
        {
            System.out.println("subclass2");
        }
      }
      class TestPolymorphism3 {
            public static void main(String[] args){
              Parent a;
              a = new subclass1();
              a.Print();
              a = new subclass2();
              a.Print();
            }
      }
      
**6. What is inheritance in OOP ?**

      Inheritance is a mechanism that allows the class to use the states and behavior of another class. In simple words a class derive 
      field and methods from another class. The derived class in inheritance is called sub class (also called derived class or extended 
      class, or child class) and the class from which it is derived is called super class (also called base class or a parent class)
      
      A super class can have any number of sub class in inheritance but sub class can only extend one super class. 
      Multiple inheritance is not supported in JAVA
      
      Types Of Inheritance :-
      
      Single Inheritance
      Multilevel Inheritance
      Hierarchical Inheritance
      
**7. Why multiple inheritance is not supported in java ?**

      To remove ambiguity:
      Multiple inheritance is not supported in java as it causes ambiguity in few scenarios. The most common scenario is Diamond problem.
        ![ambiguity-problem-in-JAVA](https://user-images.githubusercontent.com/35212651/215060953-fd0b51a8-728b-4a46-893b-db2446215cc2.jpg)
        
      Consider the above diagram which shows multiple inheritance. In this class D extends both class B & C.Here class B & C inherit 
      the same method of class A. Now the problem comes when class D is extending both class B & C and if class D wants to use same method 
      then which method would be called? That’s why multiple inheritance is not supported in java as to remove ambiguity.
      
      
**8. Use of super keywork in Inheritance. ?**

      Base.java:
      class Base
      {
           int x=50;
      }
      Child.java:
      class Child extends Base
      {
           int x=20;
           void show()
           {
                System.out.println(x);
                System.out.println(super.x);
           }
       }
       public class InheritanceAbhiAndroid{
           public static void main(String[] args)
           {
               Child c=new Child();
               c.show();
           }
       }
    
    
**9. Inheritance Important Points To Remember ?**

    1.Whenever a parent class and a child class both are having same data members then this concept is known as data hiding.
    2.Whenever a parent class and a child class both are having ditto same functions then this concept is known as method overriding.
    3.Whenever a parent class and a child class both are having same static functions then this concept is known as function hiding.
    4.We cannot print super, there is a syntax error. Always data members of parent class is inherited by super
    5.If you make any non static function of a class as final then it cannot be overridden by the child class that means to 
        stop method overriding makes a function final.
    6.Inheritance allows the class to use the states and behavior of another class using extends keyword
    7.Inheritance is-a relationship between a Base class and its child class.
    8.Multiple inheritance is not supported in JAVA.
        
**10. Can Interfaces to be extended ?**

    Yes, an interface can extend other interfaces. it supports multiple inheritances, which means it can extend more than one interface. 
    But every class which wants to use an interface must add it by keyword implements and using the keyword extends for 
    interfaces in classes is illegal and cause compile error.
    
**11. Abstraction in OOP ?**

    Abstraction is the concept of object-oriented programming that “shows” only essential attributes and “hides” unnecessary information. 
    The main purpose of abstraction is hiding the unnecessary details from the users. Abstraction is selecting data from a larger pool 
    to show only relevant details of the object to the user. It helps in reducing programming complexity and efforts. 
    It is one of the most important concepts of OOPs.

    Consider a real-life example of a man driving a car. The man only knows that pressing the accelerators will increase the speed 
    of a car or applying brakes will stop the car, but he does not know how on pressing the accelerator the speed is actually increasing, 
    he does not know about the inner mechanism of the car or the implementation of the accelerator, brakes, etc in the car. This is what abstraction is. 
   
    In java, abstraction is achieved by interfaces and abstract classes. We can achieve 100% abstraction using interfaces
   
    Abstract classes and Abstract methods :  

    1.An abstract class is a class that is declared with an abstract keyword.
    2.An abstract method is a method that is declared without implementation.
    3.An abstract class may or may not have all abstract methods. Some of them can be concrete methods
    4.A method-defined abstract must always be redefined in the subclass, thus making overriding compulsory or making the subclass itself abstract.
    5.Any class that contains one or more abstract methods must also be declared with an abstract keyword.
    6.There can be no object of an abstract class. That is, an abstract class can not be directly instantiated with the new operator.
    7.An abstract class can have parameterized constructors and the default constructor is always present in an abstract class.
   
    When to use abstract classes and abstract methods with an example

    There are situations in which we will want to define a superclass that declares the structure of a given abstraction without providing a complete 
    implementation of    every method. Sometimes we will want to create a superclass that only defines a generalization form that will be shared by 
    all of its subclasses, leaving it to each    subclass to fill in the details.

    Consider a classic “shape” example, perhaps used in a computer-aided design system or game simulation. The base type is “shape” and each shape has a color, size,       and so on. From this, specific types of shapes are derived(inherited)-circle, square, triangle, and so on — each of which may have additional characteristics and       behaviors. For example, certain shapes can be flipped. Some behaviors may be different, such as when you want to calculate the area of a shape. The type hierarchy     embodies both the similarities and differences between the shapes.

    // Java program to illustrate the
    abstract class Shape {
        String color;
        // these are abstract methods
        abstract double area();
        public abstract String toString();
        // abstract class can have the constructor
        public Shape(String color)
        {
            System.out.println("Shape constructor called");
            this.color = color;
        }
        // this is a concrete method
        public String getColor() { return color; }
    }
    class Circle extends Shape {
        double radius;
        public Circle(String color, double radius)
        {
            // calling Shape constructor
            super(color);
            System.out.println("Circle constructor called");
            this.radius = radius;
        }
        @Override double area()
        {
            return Math.PI * Math.pow(radius, 2);
        }
        @Override public String toString()
        {
            return "Circle color is " + super.getColor()
            + "and area is : " + area();
        }
    }
    class Rectangle extends Shape {
        double length;
        double width;
        public Rectangle(String color, double length,double width)
        {
            // calling Shape constructor
            super(color);
            System.out.println("Rectangle constructor called");
            this.length = length;
            this.width = width;
        }
        @Override double area() { return length * width; }
        @Override public String toString()
        {
            return "Rectangle color is " + super.getColor()
                + "and area is : " + area();
        }
    }
    public class Test {
        public static void main(String[] args)
        {
            Shape s1 = new Circle("Red", 2.2);
            Shape s2 = new Rectangle("Yellow", 2, 4);
            System.out.println(s1.toString());
            System.out.println(s2.toString());
        }
    }
    
**12. Differences between abstract classes and interfaces ?**

    An abstract class, is a class that contains both concrete and abstract methods (methods without implementations). 
    An abstract method must be implemented by the abstract class sub-classes. Abstract classes cannot be instantiated and need to be extended to be used.

    An interface is like a blueprint/contract of a class (or it may be thought of as a class with methods, but without their implementation). 
    It contains empty methods that represent, what all of its subclasses should have in common. The subclasses provide the implementation for each of these methods.       Interfaces are implemented.
    
Support multiple inheritances	Does not support multiple inheritances
Can extends another interfaces only	Can extends another class and implement multiple interfaces
Does not contain data member	Contains data member
Does not contains constructors	contains constructors
In Java Contains only incomplete member (signature of member)	Contains both signature (abstract) of method and member functions
Cannot have access modifiers by default and everything is assumed as public	Can has access modifiers for subs, methods and fields
![image](https://user-images.githubusercontent.com/35212651/215100046-d4d3b8b8-a30a-42ba-9cc7-7aaa0f107b10.png)

    
**13. What is constructor in OOP ?**

    constructors in Java is a terminology used to construct something in our programs. A constructor in Java is a special method that is 
    used to initialize objects. The constructor is called when an object of a class is created. It can be used to set initial values for object attributes. 

    In Java, a constructor is a block of codes similar to the method. It is called when an instance of the class is created. 
    At the time of calling the constructor, memory for the object is allocated in the memory. It is a special type of method which 
    is used to initialize the object. Every time an object is created using the new() keyword, at least one constructor is called.
    
    **How Constructors are Different From Methods in Java? 
    
    Constructors must have the same name as the class within which it is defined it is not necessary for the method in Java.
    Constructors do not return any type while method(s) have the return type or void if does not return any value.
    Constructors are called only once at the time of Object creation while method(s) can be called any number of times.

    **Example** :-
    class Geek
    {   
        // A Constructor
        Geek() {}
    }
    // We can create an object of the above class
    // using the below statement. This statement
    // calls above constructor.
    Geek obj = new Geek(); 
    
    **Need of Constructor**
    Think of a Box. If we talk about a box class then it will have some class variables (say length, breadth, and height). 
    But when it comes to creating its object(i.e Box will now exist in the computer’s memory), then can a box be there with 
    no value defined for its dimensions? The answer is No. 
    
    So constructors are used to assign values to the class variables at the time of object creation, either explicitly 
    done by the programmer or by Java itself (default constructor).
    
    **When Constructor is called?**
    
    Each time an object is created using a new() keyword, at least one constructor (it could be the default constructor) 
    is invoked to assign initial values to the data members of the same class. 

    Rules for writing constructors are as follows:

    The constructor(s) of a class must have the same name as the class name in which it resides.
    A constructor in Java can not be abstract, final, static, or Synchronized.
    Access modifiers can be used in constructor declaration to control its access i.e which other class can call the constructor.
    So by far, we have learned constructors are used to initialize the object’s state. Like methods, a constructor also contains a 
    collection of statements(i.e. instructions) that are executed at the time of Object creation.
    
    
     
      
      

  

  
