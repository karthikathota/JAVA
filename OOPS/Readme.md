# OOPS

Object-Oriented Programming is a methodology or paradigm to design a program using classes and objects.

### Class

Class is a user-defined data type which defines its properties and its functions.  
It can also be called as blueprint of an object.

### Object

Object is an instance of a class. An object can operate on both data members and member functions.

## Defining a class

```java
class pen{
    String color;
    String type;
    public void write()
    {
        System.out.println("Writing something");
    }
    public void info()
    {
        System.out.println("This is a "+this.color+" Pen");
    }

}
```

Here color and type are the properties of the class and write() and info() can be called as the methods of ths class.

## Creating an instance of the class

```java
public static void main(String[] args) {
pen pen1= new pen();
pen1.color="Red";
pen1.type="click";
pen1.write();
pen1.info();
}
```

Here the keyword new is a constructor whose main goal is to initialize object. They set the initial values for the object's attributes (also known as instance variables) and perform any necessary setup tasks.

# Polymorphism

Polymorphism is a fundamental concept in object-oriented programming (OOP) that allows objects of different classes to be treated as objects of a common superclass

## Compile-time Polymorphism

Also known as method overloading
Occurs when you have multiple methods in the same class with the same name but different parameters

```java
class details{
    String name;
    int age;

    public void printInfo(String name) //Method-1
    {
        System.out.println(name);
    }
    public void printInfo(int age) //Method-2
    {
        System.out.println(age);
    }
    public void printInfo(String name,int age) //Method-3
    {
        System.out.println(name + " " + age);
    }
}
```

In this based on tha parameters passed their respective method gets implemented.  
For Example

```java
details d1=new details();
d1.name="Karthik";
d1.age=24;
d1.printInfo(d1.name);
d1.printInfo(d1.age);
d1.printInfo(d1.name,d1.age);

//Output
Karthik
24
Karthik 24
```
