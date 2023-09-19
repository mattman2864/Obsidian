**Methods** are procedures that control and define the behavior of an [[Object]].
# Method Signatures
Methods have signatures that consist of the name of the method and the parameter list. A method signature for a method without parameters consists of the method name and an empty parameter list.
```java
public void printHello();
```
Each method signature has four parts:
1. **public** - The public statement tells Java which classes can see and use the method. Public methods allow other classes to call the methods, while private methods are only available to that particular class.
2. **void** - After the public or private declaration, the signature contains the return type. When a method doesn't return a value, `void` is used as the return type. Some return type or `void` is required for all methods, but not for the constructor.
3. **methodName** - After the return type, you see the name of the method. While the name can be anything, it is important to give methods names that make sense. For example, if you want a method to print the value of a rectangle width, you may name it `printWidth()` so that the user would know what to expect from the method.
4. **()** - Finally you have a set of parentheses that hold the parameter list. In this case, you have no parameters, so you include an empty set of parentheses.
# Using Methods
Methods allow programmers to perform a specific task without having to know the details of how that method was written. This is known as procedural abstraction. The programmer only needs to know what the method does, including any inputs and any outputs to the method.
## Calling Methods
When calling a method (or constructor), the call interrupts the sequential execution of statements, causing the program to first execute the statements in the method or constructor before continuing. Once the last statement in the method or constructor has been executed or a return statement is executed, the flow of control is returned to the point immediately following where the method or constructor was called.

Methods can be called from any other method, including the main method or another method in a class. How a method is called depends on the type of method that you are calling. In this section, you are going to look at calling non-static void methods. Non-static methods are called through objects of a class and you need to create an object before you can call them. In contrast, static methods can be called without creating a particular instance of an object.
# Parameters
When you want to call a method with a given input, you use parameters. For example, if you wanted to create a method called `addTen` that adds `10` to a number and prints the resulting value, you will need parameters to give a number as input.
Here is an example of an `addTen` method in [[Java]]:
```java
public void addTen(int x){
	int xPlusTen = x + 10;
	System.out.println(xPlusTen);
}
```
Notice that there is an `x` that is being taken in and used by the method. This is the parameter. Its value will be whatever the user decides to “pass” to the method. Also, note that the `x` parameter can be used as a regular variable in the body of the method.
## Calling a Method with Parameters
Now that the `addTen()` method is defined, it’s time to call the method. Let’s first add ten to the number 5:
```java
addTen(5);
```
This will result in `15` being printed to the console.
This works with variables as well. You can create a variable `y` that stores a number, then pass `y` to the `addTen` method.
```java
int y = 5;
addTen(y);
```
The variable `y` is passed as an **argument** to the `addTen()` method. The method accepts `y` as the **parameter**, adds 10 to it, and then prints `15` to the console. Note that the argument type needs to match the parameter type.
### Pass by Value
When we pass an argument to a method, it is said to be passed by value, which means a copy of that argument is made to use in the method. As a result, any change to the formal parameter will not be reflected in the actual parameters from the original calling function.

In the example below, `a` does not change value.
```java
int a = 5;
addTen(a);
System.out.println(a); // This will print 5, as the value of a did not change

public void addTen(int x){
	x += 10;
}
```
For example, if you were to write a generic `add()` method, you would want to be able to input two numbers. To include more than one parameter, you can simply write more than one parameter, separated by a comma. The method below takes in two numbers, represented by `x` and `y`, and adds them:
```java
public void add(int x, int y)
{
  int sum = x + y;
  System.out.println(sum);
}
```
You call the method in a similar manner. If you give the function the following calls:
```java
add(10, 90);
add(635, 1000);
int first = 72;
int second = 14;
add(first, second);
```
then the program will print the following to the console:
```text
100
1635
86
```
