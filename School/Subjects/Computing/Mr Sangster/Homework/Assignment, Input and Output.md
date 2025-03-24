[[Computing]][[CSharp]]
#18/9/24
## Assignment

Assignment is forming a new variable, and giving it a value.
In languages such as python, you can simply:
```python
variable = 'Hello World'
```

However, in programming languages like C#, you have to define a type of variable, otherwise the assignment will return an error.
in C# the assignment of a string containing hello world, looks like:
```csharp
string variable = "Hello World";
```

The "string" part of the assignment, defines the data type of the variable. There are many different data types. 
Such as:
float, bool, double, integer, and more...

## Input

The way to take an input to a variable in C#, is using, Console.ReadLine(), as shown below:
```csharp
string variable = Console.ReadLine();
```

However, this simple provides the user with a flashing cursor, and may confuse them as to what to input. This is where outputting is useful.

## Output

The way to print to the console in C# is using Console.WriteLine(), as shown below:
```csharp
Console.WriteLine(variable);
```

Or, you can print anything without assigning it to a variable before as shown:
```csharp
Console.WriteLine("Hello World!");
```
This can also be used with numbers:
```csharp
Console.WriteLine(123);
```

## Combining Input and Output

By combining input and output, we can provide the user with an intuitive message to prompt an input, so that they what they are inputting, and why.

To help with this, in order to get the input on the same line as the text prompt, we can use Console.Write(), instead of Console.WriteLine(). 

An example of this input method can be seen below:
```csharp
Console.Write("Please enter a number: ");
string number = Console.ReadLine();
```

## Converting Data Types When Inputting

However, there is a slight problem to the above method. Currently, the number inputted will be stored as a string, and therefore you cannot perform arithmetic calculations on it such as addition or multiplication. 

It may seem simple to switch the "string" to "int", although this does not work, as Console.ReadLine() always takes a string input.

To combat this, we can use Convert.ToInt32, to convert the string to a 32 bit integer.
There are 2 ways to do this, either in the line with the ReadLine() command, or after it.

1st Method:
```csharp
Console.Write("Please enter a number: ");
string number = Console.ReadLine();
int number = Convert.ToInt32(number);
```

2nd Method:
```csharp
Console.Write("Please enter a number: ");
string number = Convert.ToInt32(Console.ReadLine());
```

Both methods are equally valid, although the second method is more concise.