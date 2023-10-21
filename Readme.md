# JAVA

![](img/javaimg.png)

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

1. Built-in Packages.
2. User-defined Packages.

## What is java.lang.object ?

In Java, java.lang.Object is the root class for all other classes.
It is the superclass of all classes in Java and is at the top of the class hierarchy. This means
that every class in Java, either directly or indirectly, inherits from the java.lang.Object class. It provides a set of common methods and behaviors that are available to all objects in Java.
