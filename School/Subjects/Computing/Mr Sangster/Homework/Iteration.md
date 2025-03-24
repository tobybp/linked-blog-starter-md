[[Computing]]
#30/10/24
## Definite Iteration (explanation)
Definite iteration is when a program is pre-set to iterate a set number of times, and only this number of times. This is count controlled iteration, when the amount of repetition is controlled by a count, that increases or decreases every time the loop runs. 
## Indefinite Iteration (explanation)
Indefinite iteration is when a program will repeat something "indefinitely" until something happens, or stops happening. This is condition controlled iteration and therefore the number of iterations is controlled by a condition.
## For Loops (pseudocode)
A basic for loop in pseudocode would look like this:
```
For i = 1 To 5
	OUTPUT i
EndFor
```
This is a very basic pseudocode extract that would repeat 5 times and print the number inthe sequence as it goes. An example output of this would look like:
`1`
`2`
`3`
`4`
This would not include 5, as it is exclusive, going "up to" 5. not including it.
## While ... Do Loops (pseudocode)
This loopExecutes a block of code as long as a specified condition is true.

Example:
```
WHILE count < 10
	OUTPUT count
	count = count + 1 
END WHILE
```
This loop will continue running as long as `count` is less than 10, incrementing `count` by 1 each iteration.
## Repeat ... Until Loops (pseudocode)
Executes a block of code until a specified condition is true. The code inside the loop will run at least once.

Example:
```
REPEAT
	OUTPUT "Enter a positive number"
	number = INPUT 
UNTIL number > 0
```
This loop will continue asking for a positive number until `number` is greater than 0, guaranteeing at least one prompt.
## For Loops (C#)
Used for a known number of iterations.
Syntax:
```csharp
for (int i = 0; i < n; i++) 
{     
	// statements 
}
```

Example:
```csharp
for (int i = 0; i < 10; i++) 
{     
	Console.WriteLine(i); 
}
```

The loop runs from `i = 0` to `i = 9`, executing the statements within it on each iteration.
## ForEach item in collection (C#)
Iterates over each element in a collection, such as an array or list.

Example:
```csharp
int[] numbers = new [ 1, 2, 3, 4, 5 ];
foreach (int number in numbers) 
{     
	Console.WriteLine(number); 
}
```
This loop processes each item in `numbers` one by one, printing each `number`.
## While ... Do Loops (C#)
Executes a block of code as long as a specified condition is true.
Syntax:
```csharp
while (condition)
{     
	// statements
}
```

Example:
```csharp
int count = 0;
while (count < 10) 
{     
	Console.WriteLine(count);
	count++; 
}
```
This loop prints values from `count = 0` to `count = 9`, incrementing `count` until the condition `count < 10` is false.
## Do ... While Loops (C#)
Similar to `while` loops but guarantees the loop will run at least once.
Syntax:
```csharp
do 
{     
	// statements 
} while (condition);
```

Example:
```csharp
int count = 0;
do 
{     
	Console.WriteLine(count);
     count++; 
} while (count < 10);
```
This loop will execute the block first, then check the condition. `count` will print from 0 to 9.
## Nested Iteration (in general)
One loop inside another, useful for processing data structures.
Example (C#):
```csharp
for (int i = 0; i < 3; i++)
{     
	for (int j = 0; j < 3; j++)     
	{        
		Console.WriteLine($"i: {i}, j: {j}");  
	} 
}
```

The outer loop (variable `i`) runs three times. For each iteration of `i`, the inner loop (variable `j`) also runs three times, resulting in a total of 9 iterations over both loops.