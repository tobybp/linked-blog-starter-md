[[Computing]]  
#21/3/26
# Functional Programming – Lists in Functional Programming
## Recap: First-class objects
- A first-class object (or value) is something that can:
    - be in expressions
    - assigned to a variable
    - passed as an argument
    - returned from a function
- In functional programming, **functions are also first-class objects**

---
## Recap: Functions and parameters
- Functions take **one parameter at a time**
- A function with multiple parameters actually:
    - takes one argument
    - returns another function (partial application)
- Example:  
    `add :: Integer -> (Integer -> Integer)`

---
## Higher-order functions
- A higher-order function:
    - takes a function as input, or
    - returns a function, or
    - both
- Examples:
    - `map`
    - `filter`
    - `fold`

---
## What is a list?
- A **list** is a collection of elements of same type
- Written using square brackets:  
    `[1,2,3]`, `["a","b","c"]`
- A list is made of:
    - **head** → first element
    - **tail** → rest of the list

Example:
	listA = [1,2,3]  
	head listA  → 1  
	tail listA  → [2,3]

---
## Strings as lists

- A **string** is a list of characters

Example:
	word = "feast"  
	head word → 'f'  
	tail word → "east"

---
## Chasing the tail
- you can repeatedly apply `tail`
Example:
	tail (tail [1,2,3]) → [3]

---
## Empty list
- The empty list is written as:  
    `[]`
- Properties:
    - length = 0
    - contains no elements

---
## List operations
### Length
- Returns number of elements  
    Example:
		length [1,2,3] → 3

---
### Null (empty check)
- Checks if a list is empty
	Example:
		null [] → True  
		null [1] → False

---
## Prepending to a list
- Add an element to the **front** using `:`
Example:
	5 : [1,2,3] → [5,1,2,3]
- Add a list to the front using `++`
	[5,4] ++ [1,2,3] → [5,4,1,2,3]

---
## Appending to a list
- Add elements to the **end** using `++`
Example:
	[1,2,3] ++ [4,5] → [1,2,3,4,5]

---
## Immutable lists
- Lists are **immutable**:
    - Cannot be changed after creation
- Instead, create a **new list**
	Example:
		list1 = [1,2,3]  
		newList = list1 ++ [4,5]

---
## Concatenation
- Combine lists using `++`
Example:
	["fish"] ++ ["chips"] ++ ["peas"]  
	→ ["fish","chips","peas"]

---
## concat function
- Combines elements of a list into one value
	Example:
		concat ["fish"," and"," chips"]  
		→ "fish and chips"