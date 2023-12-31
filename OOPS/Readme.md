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
It is compulsory to have a differentiating factor.

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
Karthik //Method-1
24 //Method-2
Karthik 24 //Method-3
```

# Inheritance

Inheritance is a process in which one object acquires all the properties and behaviors of its parent object automatically. In such a way, you can reuse, extend or modify the attributes and behaviors which are defined in other classes.

### Single Inheritance

When one class inherits another class, it is known as single level inheritance

```java
class shape{
    String color;
}
class triangle extends shape{
     public void info()
     {
         System.out.println("It is a "+color+" triangle");
     }

}
public class Main {
    public static void main(String[] args) {
        triangle t1= new triangle();
        t1.color = "red";
        t1.info();
    }
}
```

### Multilevel inheritance

Multilevel inheritance is a process of deriving a class from another derived class

```java
class shape{
    String color;
}
class size extends shape{
    int b;
    int l;
}
class triangle extends size{
     public void info()
     {
         System.out.println("Area is "+((1.0/2)*l*b));
         System.out.println("It is a "+color+" triangle");
     }

}
public class Main {
    public static void main(String[] args) {
        triangle t1= new triangle();
        t1.color = "red";
        t1.b=4;
        t1.l=4;
        t1.info();
    }
}
```

### Hierarchical inheritance

Deriving more than one child(Sub class) class from one parent class(base class).

```java
class shape{
    String color;
}
class size extends shape{
    public void showinfo()
    {
        System.out.println("It is a big triangle");
    }

}
class triangle extends shape{
     public void info()
     {
         System.out.println("It is a "+color+" triangle");
     }

}
public class Main {
    public static void main(String[] args) {
        triangle t1= new triangle();
        t1.color = "red";
        t1.info();
        size s1= new size();
        s1.showinfo();
    }
}
```

### Hybrid inheritance

It is a combination of Single,Multilevel,Hierarchical inheritances.

## Access Modifiers

### Private

The access level of a private modifier is only within the class. It cannot be accessed from outside the class.

### Default

The access level of a default modifier is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.

### Protected

The access level of a protected modifier is within the package and outside the package through child class. If you do not make the child class, it cannot be accessed from outside the package.

### Public

The access level of a public modifier is everywhere. It can be accessed from within the class, outside the class, within the package and outside the package.
