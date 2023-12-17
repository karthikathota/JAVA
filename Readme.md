# JAVA

![](img/javaimg.png)

## JDK(Java Development Kit)

JDK is a software package that consists of the JVM, java compiler(javac) and debugger(jdb) and other essential utilities needed for developing java applications.  
Developers use the JDK to create, compile, and debug Java applications and applets.  
The JDK is necessary for writing, compiling, and testing Java code.

## JRE (Java Runtime Environment)

JRE is a software package that includes the JVM and essential libraries and components needed to run Java applications.  
It does not include development tools (like a compiler) or source code; it's designed for running compiled Java applications.

## JVM (Java Virtual Machine)

JVM is an integral part of the Java platform and is responsible for executing Java bytecode. It provides a runtime environment in which Java applications can run. JVM is platform-independent, meaning it allows Java programs to run on different operating systems without modification.  
It performs tasks such as bytecode verification, memory management, garbage collection, and just-in-time (JIT) compilation of bytecode to native machine code.

## Varaibles

```java
String user_name = "KARTHIK"
```

Here String is the type of the variable.  
**user_name** is the name of the variable.  
**KARTHIK** is the data in the variable.

They are of 2 types:-  
Primitive  
Non-Primitive

### Primitive

byte :- numbers between -128 to 127  
char  
int  
float  
char

### Non-Primitive

Strings is the best example of Non-Primitive datatype.  
Non-Primitive has built in methods for operations variables.

## RULES OF DECLARING VARIABLES

During decleration of float number we must end the value with "F" so that the compilers identifies it as an float number rather than an integer number. Same for long we must use "L" at the end of the number.

# Strings

In java strings are immutable i.e once declared cannot be edited.

## OPERATIONS ON STRINGS

Print the length of the variable.

```java
String name = "Karthik";
System.out.println(name.length());
```

Concatenate two strings

```java
String name_1 = "Karthik";
String name_2 = "Athota";
String name_3= name_1+name_2;
System.out.println(name_3);
```

char.AT() => reuturn the value at the argument passed.

```java
String name_1 = "Karthik";
System.out.println(name_1.charAt(0));
```

Replacing characters in a string.

```java
String name_1 = "Karthik";
String name_2= name_1.replace('a' , 's');
System.out.println(name_2);
```

Get substring from main string.

```java
String name_1 = "sai and karthik";
System.out.println(name_1.substring(0,3));
```

# ARRAYS

It is a non-primitive data type.

## Decalring an array

```java
int[] marks = new int[3];
marks[0]=30;
marks[1]=20;
marks[2]=10;
```

## Operations on a Array

Printing the length

```java
int[] marks = new int[3];
marks[0]=30;
marks[1]=20;
marks[2]=10;
System.out.println(marks.length);
```

Sorting an array.

```java
int[] marks = new int[3];
marks[0]=30;
marks[1]=20;
marks[2]=10;
Arrays.sort(marks);
System.out.println(marks[0]);
```

# Casting

Converting one datatype to the other

## Implicit Casting

Converting small data type to large. In implicit casting we donot loose any data.

```java
double p = 100.0;
double fp = p + 18;
System.out.println(fp);
```

## Explicit casting

In this type of casting we ask the compiler to convert larger datatypes into smaller data types even though some data might be lost.

```java
int p = 100;
int fp = p + (int)18.0;
System.out.println(fp);
```

# PACKAGES

A package in Java is used to group related classes.
Think of it as a folder in a file directory. We use packages to avoid name conflicts, and to write a better maintainable code. Packages are divided into two categories:

For EG:- In the context of name conflicts.

```
test/sai/Employee.java
test/car/Employee.java
```

In java we can find 2 types of Packages:

1. Built-in Packages.(EG:- java.lang, java.util)
2. User-defined Packages.

## What is java.lang.object ?

In Java, java.lang.Object is the root class for all other classes.
It is the superclass of all classes in Java and is at the top of the class hierarchy. This means
that every class in Java, either directly or indirectly, inherits from the java.lang.Object class. It provides a set of common methods and behaviors that are available to all objects in Java.

# ABSTRACT CLASS

Abstract classes in Java are a fundamental concept in object-oriented programming that allow you to define common behaviors and characteristics that can be inherited by subclasses.  
We cannot create an object for Abstract Classes but when can use the method defined by inheritance and polymorphism concepts.  
The main purpose of abstract class is to define some methods and which can be shared with all the realted child classes.

### ABSTRACT METHOD

Abstract method are declared in the abstract class but donot have any implementation there but are implemented in a non-abstract class or subclass.

```java

// OUTPUT

This is a student
```

# INTERFACE

In simple words an INTERFACE in java defines methods(Abstract Method only) that a class must implement if it inherits the interface. We cannot create an object for an interface. When an class does not define the method that it inherited from INTERFACE then an error will be raised.

```java
public interface hello
	{
		void hello();
		void name();
	}

	class student implements hello{
		String name;
		public student(String user)
		{
			this.name=user;
		}

		public void hello()
		{
			System.out.println("This is student");
		}
	}
```

The above code throws an error as we didnot implement all the method defined in the interface.

The proper manner to implement an INTERFACE is

```java
public interface hello {
        void message();
        void name();
    }

    class student implements hello {
        String name;

        public student(String user) {
            this.name = user;
        }

        public void message() {
            System.out.println("This is student");
        }

        public void name() {
            System.out.printf("This is %s", this.name);
        }
    }
```

# Exception Handling

Exception handling in Java is a crucial mechanism for dealing with runtime errors and unexpected situations.
It allows your program to continue execution even when something goes wrong, preventing crashes and ensuring smooth user experience.  
There can be various types of errors like  
-> User Input error  
-> File access issue  
-> Network connectivity problems  
etc.

In java there are 2 ways in whc=ich we can handle these errors during runtime.

## try-catch block

The try block contains the code that might throw an exception.  
The catch block defines how to handle specific exceptions thrown within the try block.  
You can have multiple catch blocks to handle different types of exceptions.  
If no catch block matches the thrown exception, the program terminates with an error message.

```java
try {
  int x = Integer.parseInt("abc");
}
catch (NumberFormatException e) {
  System.out.println("Invalid input: " + e.getMessage());
}
```
