[[Computing]]
#3/1/25
## The General Term sub-routines/sub-programs

- In a program, if you have a section of code that you are going to be using more than once throughout the program, you shouldn't just copy and paste the code wherever you need it. This is seen as bad practice in programming.
- Instead, you should be putting this chunk of code into a sub-routine and running the sub-routing whenever you need to use that block of code.
#### In C# these are called methods.

- In the class, we refer to the variables contained as "properties".
- So a "Person" class may have a "hairColour" property and a "walk()" method.
## Procedures, Functions and Differences Between

- The term function, is a widely misused term.
- A function is a type of sub-routine that will return data.
- This can be a certain data type such as an integer or a string.
- On the other hand, procedures do NOT return anything.
- An example of a function is `Console.ReadLine()`.
- An example of a procedure is `Console.WriteLine("").
## Declaring a Procedure and a Function

- In order to create a new procedure, you must do this:
```csharp
static void Printer()
{
	Console.WriteLine("Hello");
}
```

- To create a new function, you will need to do something with the value it returns, so in this case we will put it into a variable, then print it.
```csharp
static string GetHello()
{
	return "Hello";
}
String h = GetHello();
Console.WriteLine(h);
```
## Declaring Parameters

- We can "pass" data into a sub-routine if we want to by simply writing its data type and a temporary name within the brackets of the sub-routine's declaration. Then we can use the local variable inside of the method.
- Here is an example:
```csharp
static void Printer(string words)
{
	Console.WriteLine(words)
}
Printer(h)
```
- In this case the string variable "words" is being used as a parameter.
## Passing Data to a Sub-routine

```csharp
static void Printer(string words)
{
	Console.WriteLine(words)
}
String h = getHello(); //sets the variable h to "Hello"
Printer(h) // This will pass the data from the variable h into the sub-routine.
```
- As seen in this example previously, passing data into a subroutine can be done using parameters. In this case, the string h, is being passed into the sub-routine as a string called words.
## Returning Data
- If a sub-routine has a data type before its name, instead of the word "void", it will become a function due to it giving data back.
- For example if you have a complex set of calculations to perform, it makes sense to put it into a sub-routine in order to use it whenever you need.
- Additionally, when you want to change part of this block of code, you will only have to do it once, rather than for ever instance if you were to copy the code.
## Scope/Local Variables
- If a variable is declared within a loop/method, then the scope of the variable is local to that loop/method. 
- Whenever the loop or method ends, then the variable is terminated and discarded. It will no longer exist.
- If you want the variable to exist after the loop or method ends, then you would need to create the variable outside of the loop/method, then simply reference it, then it will still exist afterwards.
## Pass by Value
- if you pass a primitive data type to a method, it makes a copy of the value of that data into memory somewhere, then creates a new temporary variable name, that points to the data in memory where the variable with the name in the method declaration is pointing to. 
- This way the two variables initially have the same value, but are completely separate, so if you change one of them, the other does not change.
- These are commonly called value types.
#### Examples of primitive data types that can be used with this:
- int
- string
- double
- boolean
- long
- char
- float
## Pass by Reference in Lists/Arrays
- If you pass a complex data type into a method, then it creates a new temporary variable name that points to the original data in memory matching the name in the method declaration.
- This means that you can change that data.
- These are commonly called reference types.
#### Examples of complex data types that can be used with this:
- Arrays of any data type
- ArrayList 
- List
- Dictionary
- DateTime
- File
- StreamReader
- StreamWriter
- BigInteger
- Any custom classes that you create.
## Using ref in C\#
- Using `ref` will force a primitive data type passed in to be a reference rather than a value.

```csharp
static void RefChanger(ref int c)
{
	c = c + 1;
}
int b = 0;
RefChanger(ref b);
Console.WriteLine(b);
```
## Using out in C\#

- `d` will point to a location in memory. `c` cannot look at the value of `d`, even though it has been passed into the sub-routine. `c` is simply a space that data can be put into.
- For example:

```csharp
static void OutChanger(out int c)
{
	c = 1;
}
int d = 0;
OutChanger(out d);
Console.WriteLine(d);
```
