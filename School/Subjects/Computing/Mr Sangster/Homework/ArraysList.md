[[Computing]]
#25/11/24

## What is an ArrayList in C\#
An ArrayList is a collection class in C# that allows dynamic resizing and stores elements as objects. Unlike traditional arrays, which have a fixed size, an ArrayList automatically gets bigger or smaller as elements are added or removed. 
## Creating an ArrayList
When you create an ArrayList, no size needs to be specified, as it dynamically adjusts.
##### Pseudocode:
```
Declare ArrayList myArrayList 
Set myArrayList = new ArrayList()
```
##### C# Code:
```csharp
ArrayList myArrayList = new ArrayList();
```
## Adding
You can add elements of any type to the ArrayList using the `Add` method. The ArrayList automatically resizes as elements are added. The element is added to the end of the arraylist.
##### Pseudocode:
```
Call myArrayList.Add("Apple") Call myArrayList.Add(42)
```
##### C# Code:
```csharp
myArrayList.Add("Apple"); // Would add a string 
myArrayList.Add(42); // Would add an integer
```
## Inserting
The `Insert` method allows you to add an element at a specific position in the ArrayList. All subsequent elements are shifted to the right.
##### Pseudocode:
```
Call myArrayList.Insert(1, "Cheese")
```
##### C# Code:
```csharp
myArrayList.Insert(1, "Cheese");
```
This inserts the string "cheese" at position 1.
## Getting a Value
You can retrieve an element from an ArrayList using its index. Bear in mind that ArrayLists start their indexes at 0.
##### Pseudocode:
```
Set value = myArrayList[1]
```
##### C# Code:
```csharp
object value = myArrayList[1];
Console.WriteLine(value); // Outputs: Cheese
```
## Removing by Search
The `Remove` method removes the first appearance of a specified element from the ArrayList.
If it doesn't find the value, the list does not change.
##### Pseudocode:
```
Call myArrayList.Remove("Apple")
```
##### C# Code:
```csharp
myArrayList.Remove("Apple"); // Removes "Apple" if it exists
```
## Removing by Index
Use the `RemoveAt` method to remove an element at a specific index. Elements following the value removed will do one shift left. Index must not be out of bounds.
##### Pseudocode:
```
Call myArrayList.RemoveAt(0)
```
##### C# Code:
```csharp
myArrayList.RemoveAt(0); // Removes the element at index 0
```
## Looping Through an ArrayList
You can loop through an ArrayList using a `for` loop or a `foreach` loop to access each element.
- **`foreach` loop**: Iterates through each element without needing to manage indices.
- **`for` loop**: Allows index-based control over iteration.
##### Pseudocode:
```
For each item in myArrayList 
Output item 
End For
```
##### C# Code (foreach):
```csharp
foreach (object item in myArrayList) 
{ 
	Console.WriteLine(item); // Outputs each item in the ArrayList 
}
```
##### C# Code (for):
```csharp
for (int i = 0; i < myArrayList.Count; i++) 
{ 
	Console.WriteLine(myArrayList[i]); // Outputs each item by index 
}
```