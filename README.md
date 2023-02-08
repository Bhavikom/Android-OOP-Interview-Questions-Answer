# Android-OOP-Interview-Questions-Answer


**1. Java - What is OOP ?**

	OOP stands for Object-Oriented Programming.

	Procedural programming is about writing procedures or methods that perform operations on the data, while object-oriented 
    	programming is about creating objects that contain both data and methods.

	Object-oriented programming has several advantages over procedural programming:

	OOP is faster and easier to execute
	OOP provides a clear structure for the programs
	OOP helps to keep the Java code DRY "Don't Repeat Yourself", and makes the code easier to maintain, modify and debug
	OOP makes it possible to create full reusable applications with less code and shorter development time
	Tip: The "Don't Repeat Yourself" (DRY) principle is about reducing the repetition of code. 
	You should extract out the codes that are common for the application, and place them at a single place and reuse them instead 
	of repeating it.
    
**2. What is an Object ?**

    An object is an instance of a class that has states and behaviors. A Class can be defined as a template that describes 
    the behavior/state that the object of its type support.
    
**3. What is the main feature of OOP ?**

    Encapsulation, Polymorphism, Inheritance, Abstraction
    
**4. What is encapsulation ?**

    Encapsulation is one of the four fundamental OOP concepts. It is a mechanism of wrapping the data (variables) and code acting 
    on the data (methods) together as a single unit. In encapsulation, the variables of a class will be hidden from other classes, 
    and can be accessed only through the methods of their current class. Therefore, it is also known as data hiding. To achieve encapsulation in Java:

    Declare the variables of a class as private.
    Provide public setter and getter methods to modify and view the variables values.
    Benefits of Encapsulation:

    The fields of a class can be made read-only or write-only.
    A class can have total control over what is stored in its fields.
  
**5. What is Polymorphism ?**

    The word polymorphism means having many forms. In simple words, we can define polymorphism as the ability of a message to be displayed 
    in more than one form. In Java polymorphism is mainly divided into two types: compile-time and runtime polymorphism.
  
**6. What is the difference between static and dynamic Polymorphism ?**
  
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
      
**7. What is inheritance in OOP ?**

      Inheritance is a mechanism that allows the class to use the states and behavior of another class. In simple words a class derive 
      field and methods from another class. The derived class in inheritance is called sub class (also called derived class or extended 
      class, or child class) and the class from which it is derived is called super class (also called base class or a parent class)
      
      A super class can have any number of sub class in inheritance but sub class can only extend one super class. 
      Multiple inheritance is not supported in JAVA
      
      Types Of Inheritance :-
      
      Single Inheritance
      Multilevel Inheritance
      Hierarchical Inheritance
      
**8. Why multiple inheritance is not supported in java ?**

      To remove ambiguity:
      Multiple inheritance is not supported in java as it causes ambiguity in few scenarios. The most common scenario is Diamond problem.
        ![ambiguity-problem-in-JAVA](https://user-images.githubusercontent.com/35212651/215060953-fd0b51a8-728b-4a46-893b-db2446215cc2.jpg)
        
      Consider the above diagram which shows multiple inheritance. In this class D extends both class B & C.Here class B & C inherit 
      the same method of class A. Now the problem comes when class D is extending both class B & C and if class D wants to use same method 
      then which method would be called? That’s why multiple inheritance is not supported in java as to remove ambiguity.
      
      
**9. Use of super keywork in Inheritance. ?**

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
    
    
**10. Inheritance Important Points To Remember ?**

    1.Whenever a parent class and a child class both are having same data members then this concept is known as data hiding.
    2.Whenever a parent class and a child class both are having ditto same functions then this concept is known as method overriding.
    3.Whenever a parent class and a child class both are having same static functions then this concept is known as function hiding.
    4.We cannot print super, there is a syntax error. Always data members of parent class is inherited by super
    5.If you make any non static function of a class as final then it cannot be overridden by the child class that means to 
        stop method overriding makes a function final.
    6.Inheritance allows the class to use the states and behavior of another class using extends keyword
    7.Inheritance is-a relationship between a Base class and its child class.
    8.Multiple inheritance is not supported in JAVA.
        
**11. Can Interfaces to be extended OR Can an Interface implement another Interface ?**

    Yes, an interface can extend other interfaces. it supports multiple inheritances, which means it can extend more than one interface. 
    But every class which wants to use an interface must add it by keyword implements and using the keyword extends for 
    interfaces in classes is illegal and cause compile error.
    
**12. Abstraction in OOP ?**

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
    all of its subclasses, leaving it to each subclass to fill in the details.

    Consider a classic “shape” example, perhaps used in a computer-aided design system or game simulation.
    The base type is “shape” and each shape has a color, size, and so on. From this, specific types of shapes are derived(inherited)-circle, 
    square, triangle, and so on — each of which may have additional characteristics and behaviors. For example, certain shapes can be 
    flipped. Some behaviors may be different, such as when you want to calculate the area of a shape. The type hierarchy embodies both 
    the similarities and differences between the shapes.

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
    
**13. Differences between abstract classes and interfaces ?**

	As we know that abstraction refers to hiding the internal implementation of the feature and only showing the functionality 
	to the users. i.e. what it works (showing), how it works (hiding). Both abstract class and interface are used for abstraction, 
	henceforth Interface and Abstract Class are required prerequisites.    
	
	To differensiate them read below points:
	
	1. Abstract classes are not fully abstract class can have both abstract as well as non abstract methods and non abstract
	methods make it partial abstraction, where interface can have only abstract methods so it gives full abstraction.
	
	2. An abstract class, is a class that contains both concrete and abstract methods (methods without implementations). where
	interface contain only abstract methods.
	
	3. From Java 8, Abstract classes can have default and static methods also. From Java 9, it can have private concrete methods as well,
	where interface contain only abstract methods.
	
	4. Variables declared in a Java interface are by default final. An abstract class may contain non-final variables.
	
	5. Abstract class can have final, non-final, static and non-static variables. The interface has only static and final variables.
	
	6. Abstract class can provide the implementation of the interface. Interface can’t provide the implementation of an abstract class.
	
	7. An interface can extend one or more Java interfaces; an abstract class can extend another Java class and implement multiple Java interfaces.
	
	8. Members of a Java interface are public by default. A Java abstract class can have class members like private, protected, etc.
	
	9. Abstract classes cannot be instantiated and need to be extended to be used where we can create instant of interface class.
   
**14. What is constructor in OOP ?**

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
    
    Types of Constructors in Java
    
    1.No-argument constructor = A constructor that has no parameter is known as the No-argument or Zero argument constructor. 
    If we don’t define a constructor in a class, then the compiler creates a constructor(with no arguments) for the class. 
    And if we write a constructor with arguments or no arguments then the compiler does not create a default constructor
    
    2.Parameterized Constructor = A constructor that has parameters is known as parameterized constructor. If we want to 
    initialize fields of the class with our own values, then use a parameterized constructor.
    
    3.Default Constructor =  A constructor that has no parameters is known as default the constructor. A default constructor is invisible. 
    And if we write a constructor with arguments or no arguments then the compiler does not create a default constructor. 
    It is taken out. It is being overloaded and called a parameterized constructor. The default constructor changed into the parameterized constructor. 
    But Parameterized constructor can’t change the default constructor.
    
**15. What is the difference between a constructor and a method ?**

    1.The name of the constructor is same as that of the class name, whereas the name of the method can be anything.

    2.There is no return type of a constructor.

    3.When you make an object of a class, then the constructor of that class will be called automatically. But for methods, we need to call it explicitely.

    4.Constructors can't be inherited but you can call the constructor of the parent class by calling super().

    5.Constructor and a method they both run a block of code but the difference is in calling them.

    6.We can call method directly using their name.
    
 **16. How to prevent a class to be extended ?**

    simply use keyword final in definition of class or methods. for example:
	
 **17. Runtime polymorphism or Dynamic Method Dispatch or Method Overriding ?**
 
    Polymorphism in Java is a concept by which we can perform a single action in different ways.

    Runtime polymorphism or Dynamic Method Dispatch is a process in which a call to an overridden method is resolved 
    at runtime rather than compile-time.
    
    In this process, an overridden method is called through the reference variable of a superclass. The determination
    of the method to be called is based on the object being referred to by the reference variable.

    Let's first understand the upcasting before Runtime Polymorphism.

   *Upcasting
    
    If the reference variable of Parent class refers to the object of Child class, it is known as upcasting. For example:
     
    class A{}  
    class B extends A{}  
    A a=new B();//upcasting  
    
   *Java Runtime Polymorphism Example
   
   Consider a scenario where Bank is a class that provides a method to get the rate of interest. However, the rate of interest 
   may differ according to banks. For example, SBI, ICICI, and AXIS banks are providing 8.4%, 7.3%, and 9.7% rate of interest.
   
   Example : 
   
   class Bank{  
	float getRateOfInterest(){return 0;}  
   }  
   class SBI extends Bank{  
        float getRateOfInterest(){return 8.4f;}    
   }   
   class ICICI extends Bank{  
        float getRateOfInterest(){return 7.3f;}  
   }  
   class AXIS extends Bank{  
        float getRateOfInterest(){return 9.7f;}  
   }  
   class TestPolymorphism{  
        public static void main(String args[]){  
        Bank b;  
        b=new SBI();  
        System.out.println("SBI Rate of Interest: "+b.getRateOfInterest());  
        b=new ICICI();  
        System.out.println("ICICI Rate of Interest: "+b.getRateOfInterest());  
        b=new AXIS();  
        System.out.println("AXIS Rate of Interest: "+b.getRateOfInterest());  
        }  
   }  
      

  

  
