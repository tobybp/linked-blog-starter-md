[[Computing]]
#9/2/26 
# Functional Programming – Function Application
## First-class objects
- A first-class object (or value) is something that can:
    - appear in expressions
    - be assigned to a variable
    - be passed as an argument to a function
    - be returned from a function
- In functional programming languages such as Haskell, **functions themselves are first-class objects**

---
## Function application
- Function application is the process of supplying arguments to a function
- Although a function may appear to take multiple arguments, **a function actually takes only one argument at a time**
Example:
	`add3Integers x y z = x + y + z`
Type declaration:
	`add3Integers :: Integer -> Integer -> Integer -> Integer`
More accurately:
`add3Integers :: Integer -> (Integer -> (Integer -> Integer))`

---
## One argument at a time
When evaluating:
`add3Integers 2 4 5`
This happens in stages:
1. `add3Integers 2` returns a new function
2. That function is applied to `4`, returning another function
3. That function is applied to `5`, producing the final value

---
## Partial function application
- Partial function application occurs when a function is given **fewer arguments than it expects**
- Instead of returning a value, it returns a **new function** waiting for the remaining arguments

Example:
	`add :: Integer -> Integer -> Integer add x y = x + y`
Partial application:
	`addSix :: Integer -> Integer addSix = add 6`
Usage:
	`addSix 10`
This is same as:
	`add 6 10`

---
## Example of partial application
	`times x y z = x * y * z`
Fixing one argument:
	`poolVol l w = times 2.6 l w`
This allows reuse of a function with a fixed value.

---
## Higher-order functions
- A higher-order function is a function that:
    
    - takes a function as an argument, or
        
    - returns a function as a result, or
        
    - does both
        

Examples:

- `map`
    
- `filter`
    
- `fold`
    

---

## The map function

- `map` applies a function to every element in a list
    
- It returns a new list containing the results
    

Syntax:

`map function list`

Example:

`map (*2) [1, 2, 3]`

Result:

`[2, 4, 6]`

---

## Map with partial application

Example:

`map (max 3) [1,2,3,4,5]`

Result:

`[3,3,3,4,5]`

---

## The filter function

- `filter` selects elements from a list that satisfy a condition
    
- The condition is a **predicate** (a function that returns True or False)
    

Syntax:

`filter predicate list`

Example:

`filter (>6) [2,5,6,8,9]`

Result:

`[8,9]`

---

## Custom predicates with filter

Example:

``isEven n = n `mod` 2 == 0``

Usage:

`filter isEven [1,2,3,4,5,6]`

Result:

`[2,4,6]`

---

## Fold (reduce) functions

- A fold function reduces a list to a **single value**
    
- It does this using recursion
    
- Common uses include summing or multiplying list elements
    

---

## foldl and foldr

### foldl (fold left)

- Processes the list from left to right
    

Example:

`foldl (+) 0 [2,3,4,5]`

Equivalent to:

`(((0 + 2) + 3) + 4) + 5`

---

### foldr (fold right)

- Processes the list from right to left
    

Example:

`foldr (+) 0 [2,3,4,5]`

Equivalent to:

`2 + (3 + (4 + (5 + 0)))`

---

## When order matters

With division:

`foldl (/) 100 [2,5]`

Result:

`10.0`

`foldr (/) 100 [2,5]`

Result:

`40.0`