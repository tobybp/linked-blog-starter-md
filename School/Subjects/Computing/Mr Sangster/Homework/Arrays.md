[[Computing]]
#25/11/24

## Arrays and Indexes (general)
- An array can be defined as a finite, ordered set of elements of the same type. For example integer, real or char (characters). 
- "Finite" means that there will be a specific number of elements within that array. 
- The "ordered" implies that there is a first, second, third, last element of the array. 
- The index is the ordinal number pointing to the position in the array of the data.
## Arrays VS Lists
Lists can be dynamically changed in size, so that they can be appended to and adjust their size accordingly. This means that arrays are finite, and lists are infinite. They also have different names, with one being called an array and the other called a list.
## Declaring an Empty Array (C#)
Format:
```
<dataType>[] <variableName> = new <dataType>[<size>];
```

Example:
```csharp
int[] array1 = new int[5];
```
This creates an integer array with 5 bits of data within it. Because the array is empty, they will be each be assigned 0 to begin.
## Declaring an Array with Predefined Data (C#)
Initialising an array with values can be done like this:
```csharp
int[] numbers = new int[5] {1, 2, 3, 4, 5};
```
the "int[5]" represents how long the array is, and the contents of the curly brackets define what the values are.
The syntax would look like:
```
<dataType>[] <variableName> = new <dataType>[<size>] {content1, content2 ...};
```
## Looping Through an Array with a For Loop (C#)
To loop through an array with a for loop, you basically just use a regular for loop, with the length set to the length of the array you wish to iterate through.
For example:

```csharp
string[] cars = {"McLaren", "Lamborghini", "Ford", "Apollo"};
for (int i = 0; i < cars.Length; i++) 
{
  Console.WriteLine(cars[i]);
}
```
The first section of declaring the for loop, `int i = 0`, creates a variable called i, that we can use to count the number of times we have looped through, and keep track. The next section, `i < cars.Length` tells us that the for loop should run until i is no longer less than the length of our `cars` array. And finally, the `i++` instructs the program to add 1 to i every time it iterates through.
This program would simply output each car brand on their own line, in the order they are in the array:
`Mclaren`
`Lamborghini`
`Ford`
`Apollo`
## array.length (C#)
In C sharp, we can use the function array.Length to find the integer value for the length of the array.
The syntax for this operation can be seen as:
```
<variableType> <variableName> = <arrayName>.Length;
```

For example:
```csharp
int numOfNums = numbers.Length;
```
## IndexOutOfBoundsException
The exception that the index of out of bounds, simply means that the position in the array you have requested does not exist. For example asking for `array[7]` (8th position) when the array is only 6 long. This action would return an IndexOutOfBoundsException. This is commonly seen when in a for loop, the user uses a less than or equal to sign, instead of a less than sign to choose when to stop the iteration. This is an understandable error, as it would make sense to go "up to and including the 8th value", but that is not what you are doing, as arrays start with an index of 0, so the 8th value is actually pointed to with the number 7.
## Multidimensional arrays (arrays of arrays) (C# and general)
In general, multidimensional arrays are simply arrays inside of arrays, or an array of arrays. Think of a regular 1 dimensional array as a singular row, and as many columns s the array is long. Now think of having another dimension to this array variable, more rows, each row has columns, therefore making it a multidimensional array.

Creating a multidimensional array looks like this:
```csharp
int[,] numbers = { {1, 4, 2}, {3, 6, 8} };
```

In a table setup, this 2D array would look like this:

|       | 0   | 1   | 2   |
| ----- | --- | --- | --- |
| **0** | 1   | 4   | 2   |
| **1** | 3   | 6   | 8   |

To declare an empty 2D array of a certain size, you can do this:
```csharp
int[ , ] bigArray = new int [2,3];
```
This creates a 2D array with 2 elements, and each of those 2 elements also has 3 elements
## Getting the Length of the Inner Array (GetLength)
To get the length of one of the inner arrays, you can do this:
```
<variable> = <array>.GetLength(position)
```

For example:
```csharp
innerLength = biggerArray.GetLength(1);
```
This would get the length of the second array from the 2D array.
## Looping Through 2D Arrays
To loop through 2D arrays, you will often used nested iteration. This is usually when you have a for loop inside of a for loop, then parse the values using the count variables.
For example:
```csharp
int[ , ] numbers = { {1, 3, 4, 6} , {5, 8, 3, 2} };
for (int i = 0; i < numbers.Length; i++) 
{
  for (int j = 0; j < numbers.GetLength(i); j++)
  {
	Console.WriteLine("Row " + i+1 + ", Column " + j+1 + " is: " + numbers[i,j])
  }
}
```

This program should output:
`Row 1, Column 1 is: 1`
`Row 1, Column 2 is: 3`
`Row 1, Column 3 is: 4`
`Row 1, Column 4 is: 6`
`Row 2, Column 1 is: 5`
`Row 2, Column 2 is: 8`
`Row 2, Column 3 is: 3`
`Row 2, Column 4 is: 2`