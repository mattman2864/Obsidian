#CS
Classes are formal implementations of objects, similar to a blueprint or template. Classes are used to create objects. To create an object, you must first instantiate the object with a data type (class), and then initialize it.
# Parts of a Class
There are 3 main parts to any class:
## Instance Variables
The instance variables, or attributes, hold the state of the object. These are declared at the beginning of the class. When declaring them, they are typically declared as private, which means they are only accessible within the class.

Instance variables are not usually initialized when you declare them. For primitive variables, that means that these variables are created with default values. When an object has not been created, or [[Instantiation|instantiated]], it isn't pointing to any particular object data. When that happens, the object, in this case, is considered to be a null object. The keyword `null` is a special value used to indicate that a reference variable is not associated with any object.
## Constructor
The constructor is used to instantiate - create an instance of - an object. Any time a new object is created, the constructor is run. Notice that the constructor has a different header compared to other methods. The constructor header has the same name as the class, is always declared public, and has no return type. A class contains constructors that are invoked to create objects.
## Methods
The third part of the class is methods. These make up the behaviors of the object. There can be a number of methods, some of which take an input, some of which return a value, and some of which do both or neither.
## Method Signatures and Parameters
The first line of the constructor is known as the method signature. A **signature** consists of the constructor name and the parameter list. In the example below, the signature name is `Rectangle` and the parameter list includes `rectWidth` and `rectHeight`.
```java
public Rectangle(int rectWidth, int rectHeight)
{
	width = rectWidth;
	height = rectHeight;
}
```
The **parameter list**, in the header of a constructor, lists the types of the values that are passed in and their variable names. These are often referred to as formal parameters. Parameters allow values to be passed into the constructor to establish the initial state of the object.

To create a new rectangle, call the constructor and pass values that correspond to the parameter list. For example, to create a rectangle with a width of 5 and a height of 3, you would call it from the `main` function like this.
```java
Rectangle rect = new Rectangle(5, 3);
```
In the above example, the `5` and `3` are known as arguments. An **argument** is a value that is passed into a constructor (or any method) when called. These are often referred to as actual parameters. The actual parameters passed into a constructor must be compatible with the types identified in the formal parameter list.

Arguments are passed to the object using call by value. Call by value initializes the formal parameters with *copies* of the actual parameters.