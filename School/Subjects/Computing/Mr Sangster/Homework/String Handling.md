[[Computing]]
#15/10/24 
## Strings
A string is a sequence of characters that can be manipulated using various built-in methods or functions in C#.
```csharp
// Assignment:
string name = "Jeff";
```

In pseudocode, this would be:
```
name <- "Jeff"
```
## Length
The length of a string refers to the total number of characters in a string. This includes spaces.
The length of a string can be found by doing this in C#:
```csharp
int length = name.Length();
```
This stores the integer for length in a variable titled "length".

The equivalent code in pseudocode would be:
```
length <- len(name)
```
## Concatenation
Concatenation of a string is the process of joining two or more strings together.
Example in C#:
```csharp
string fullName = firstName + lastName;
```

You could also use various other methods of combining strings, such as formatting methods using the $ in C#:
```csharp
string fullName = ($"{firstname} {lastName}")
```
This method is ideal if you want to ensure that you have a space between the variables, or that you want to have text in between them.

In pseudocode this would be:
```
fullName <- firstName + lastName
```
## IndexOf
IndexOf determines the position of a substring within a string.
Example in C#:
```csharp
int position = name.IndexOf("ef");
```
This would store the integer value of 1, in the position variable. This is due to "ef" coming in the second letter of "Jeff". Although it may seem weird to use 1 to denote the second letter of a string, this is due to C# starting from 0 when counting, therefore the first letter would be represented by 0.

The equivalent of this in pseudocode is:
```
position <- name.find("ef")
```
## Substring
The substring method is used to extract a portion of a string based on an index position provided.
In C# this is done by:
```csharp
string endOfName = name.Substring(2);
```
This will create a new string called endOfName, containing the original string, from the value provided. In this case it would provide from the 3rd character onwards (inclusive).

For single characters, you can use a different string method:
```csharp
char secondChar = name[1];
```
This would provide a new variable "secondChar" with 'e', as e is the second letter in Jeff.

In pseudocode, it would look like this:
```
endOfName <- name.Substring(2)
secondChar <- name[1]
```
## Replace
Replace substitutes one part of a string with another.
An example of this in C#:
```csharp
string newName = name.Replace("ff", "nnifer");
```
This would replace the "ff", in the word Jeff, with "nnifer". The newName variable will be "Jennifer". You can use this method to either create a new variable using another, or to overwrite an existing variable with a replaced version of it.

In pseudocode, this would be:
```
newName <- name.replace("ff", "nnifer")
```
## ToLower
The ToLower function can be used to convert an entire string to lowercase.
In C#, this looks like:
```csharp
string lowercaseName = name.ToLower();
```
This would make the lowercaseName variable "jeff" rather than "Jeff". Similarly to replace, you can use this to convert a string to lowercase, or create a new string that is the lowercase version of another string.

In pseudocode, this is:
```
lowercaseName <- name.ToLower()
```
## ToUpper
Basically the opposite of ToLower().
This would take the "Jeff" string and make it "JEFF".
In C# This looks like:
```csharp
string uppercaseName = name.ToUpper();
```

In pseudocode, this is:
```
uppercaseName <- name.ToUpper()
```
## Trim
Trim is used to remove leading and trailing whitespace, or other specified characters from the selected string.
For example:
In pseudocode, this is:
```csharp
string trimmedName = name.Trim();
```
If there were any spaces either side of the name, this would remove them.