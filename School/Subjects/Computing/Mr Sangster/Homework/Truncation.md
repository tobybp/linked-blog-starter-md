[[Computing]]
#17/10/24 
## Parse and Convert to int and double

Parse: Converts a string to a numeric type. Throws an exception if the conversion fails.
	Example:
```csharp
int number = int.Parse("123");
double dblNumber = double.Parse("123.45");
```

Parameters: Takes a string representing a valid number.
    - **Returns**: The parsed integer or double.
    - **Exception**: Throws `FormatException` if the string is not numeric.

Convert: Safely converts types, allows `null` values.
	Example:
```csharp
int number = Convert.ToInt32("123");
double dblNumber = Convert.ToDouble("123.45");
```

Parameters: Accepts many types, including strings, booleans, etc.
    - Returns: An integer or double.
    - Exception: Throws `InvalidCastException` or `FormatException`.

## TryParse

TryParse: Similar to `Parse`, but doesn’t throw exceptions. Returns a boolean indicating success or failure.
     Example:
```csharp
int number;
bool success = int.TryParse("123", out number);
```
Parameters: Takes a string to parse and an `out` variable to store the result.
Returns `True` if successful, otherwise `False`.

## primitiveVariable.toString()

Converts primitive types (like int, double) to strings.
     Example:
```csharp
int number = 123;
string strNumber = number.ToString();
```
Parameters: Optional format strings.
Returns a string representation of the number.

## complexDataType.toString()

- Used to provide a string representation of a complex object. Can be overridden for custom output.
    - Example:
```csharp
class Person {
    public string Name { get; set; }
    public override string ToString() {
        return $"Name: {Name}";
    }
}
```
Returns an array of substrings.

## String.Split()
Splits a string into an array based on a "delimiter".
	Example:
```csharp
string sentence = "hello,world";
string[] words = sentence.Split(',');
```
Parameters: Delimiter (comma, space, and more).
Returns an array of substrings.

## String.toCharArray()
Converts a string into an array of characters.
	Example:
```csharp
string word = "hello";
char[] letters = word.ToCharArray();
```

## String.Join()
Combines elements of an array into a single string, separated by a delimiter.
	Example:
```csharp
string[] words = { "hello", "world" };
string sentence = String.Join(" ", words);
```
Returns a combined string.

## Forced Casting
Casting forces data from one type to another. 
	Example:
```csharp
double num = 123.45;
int castedNum = (int)num;  // Truncated to 123
```
Can cause runtime errors if casting between incompatible types.
Casting is deliberate when converting data, and truncation can occur when dividing integers and forcing them into other types.

## Exceptions When Casting
These occur when casting between incompatible data types.
	example:
```csharp
object obj = "123";
int number = (int)obj; // InvalidCastException
```
This will output an "InvalidCastException" error.