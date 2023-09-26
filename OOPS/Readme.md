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
