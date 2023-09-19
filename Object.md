# Overview
Objects are variables of user-defined data types, a.k.a. "reference type variables". Reference types must be declared and initialized before use. The initialized form of a reference type is referred to as an object.
# Objects
Objects are structures that contain a state and a behavior.
## State
The state contains information about a specific object.
## Behavior
The behavior is the actions that can be performed on a specific object.
# [[Classes]]
Classes are templates for objects.
Here is an example of a class that lets us create a [[Rectangle]], and get its [[Area]] in [[Java]]:
```java
public class Rectangle
{
  private double width;
  private double height;

  public Rectangle(double rectWidth, double rectHeight)
  {
    width = rectWidth;
    height = rectHeight;
  }

  public int getArea()
  {
    return width * height;
  }
}
```
## [[Classes]] vs Objects
It is important to remember that classes are just templates for creating new objects. A class is a formal implementation, or blueprint, of the attributes and behaviors of an object. An object, on the other hand, is a specific [[Instantiation|instance]] of a class with defined attributes. Objects contain both a state and a behavior, and are an instance of a class.

# Creating an Object
Every object is created using a call to the class' constructor. The call to the constructor must contain the list of parameters that match the formal parameters. Once you create a new object, the computer allocates memory for this object. Unlike primitive variables that store the object address, the memory associated with a variable of the reference type holds an object reference value or, if there is no object, `null`. This value is the memory address of the referenced object.
## Constructor Overload
To create an object, the arguments need to match the formal parameters, but what if you want to specify a different set of parameters? For example, you want to create a square and only provide side length.

In [[Java]], you can do this with what is called a constructor overload. Let's take a look at an example:
```java
public class Rectangle
{
  private int width;
  private int height;
  public Rectangle(int rectWidth, int rectHeight)
  {
    width = rectWidth;
    height = rectHeight;
  }
  public Rectangle(int sidelength)
  {
    width = sidelength;
    height = sidelength;
  }
}
```
Constructors are said to be overloaded 

