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
      
**8. Use of super keywork in Inheritance **

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
    
**9. Inheritance Important Points To Remember: **

        1.Whenever a parent class and a child class both are having same data members then this concept is known as data hiding.
        2.Whenever a parent class and a child class both are having ditto same functions then this concept is known as method overriding.
        3.Whenever a parent class and a child class both are having same static functions then this concept is known as function hiding.
        4.We cannot print super, there is a syntax error. Always data members of parent class is inherited by super
        5.If you make any non static function of a class as final then it cannot be overridden by the child class that means to 
          stop method overriding makes a function final.
        6.Inheritance allows the class to use the states and behavior of another class using extends keyword
        7.Inheritance is-a relationship between a Base class and its child class.
        8.Multiple inheritance is not supported in JAVA.
        
**10. 
    
     
      
      

  

  
