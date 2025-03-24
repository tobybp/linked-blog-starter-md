[[Computing]]
#7/10/24

There are two ways that you can represent time:
1. "Human Time". This uses the year, month, day, hour, minute and second. 
	For example: 
	10:47 07/10/24
2. "Machine Time" This measures time using an origin, called the "epoch". Machine time uses a set resolution. For example it could use milliseconds.
## Epoch C\#
- C# uses the "DateTime" class to work with date and time.
- The "Epoch" is the time elapsed since a specific starting point. In C sharp, the starting point for this is 1/1/0001 12:00 am. 
- Normally, in other languages the epoch is at January 1st, 1970.
- By default, C# will provide the user with ways in which to switch between the formatted, readable "human time" and epoch time.
## C\# DateTime
in C sharp, The object DateTime is used to handle the date and time. There are various commands in order to manipulate the date and time, such as finding the difference between two times, and the time since certain points.
## DateTime Creation and Use
To create a DateTime object, use the DateTime keyword with various constructors.
```csharp
DateTime dt = new DateTime();
```
This line will create a DateTime object that has the value from January the 1st, 0001, 00:00:00
You can specify year, month, day, hour, minute, second, and timezone in this command using various constructors.
The DateTime Class 7 properties: Hour, Minute, Second, Millisecond, Year, Month and Day.
The class also includes methods in order to extract a property, add an amount of time to the a date, and find the difference between dates.
There are also methods for parsing strings as DateTime objects, and vice versa, by formatting DateTime into strings.
Example:
```csharp
// Create a DateTime object
DateTime dt = new
DateTim(2024,10,7,11,13,19);

//Access it's properties
int year - dt.Year; // Get the year
int month - dt.Month; // Get the month
int day - dt.Day; // Get the day
int hour - dt.Hour; // Get the hour
int minute - dt.Minute; // Get the minute
int second - dt.Second; // Get the second

double timestamp = 1550545864; // Example epoch time
DateTime start = new DateTime(1970, 1, 1, 0, 0, 0, 0); // Defines the start time
start = start.AddSeconds(timestamp); // Add the seconds to the start DateTime
Console.WriteLine(start); // Output: 2/19/2019 3:11:04 AM
```
## TimeSpan 
To work out a timespan, you subtract the start time from the current time:
```csharp
TimeSpan t = DateTime.Now - new DateTime(0);
int secondsSinceEpoch = (int)t.TotalSeconds;
Console.WriteLine(secondsSinceEpoch);
// Output:1550290604
```
C sharp has a built in method for this, called TimeSpan:
```csharp
// Define two dates. 
DateTime date1 = new DateTime(2010, 1, 1, 8, 0, 15); 
DateTime date2 = new DateTime(2010, 8, 18, 13, 30, 30); 
// Calculate the interval between the two dates. 
TimeSpan interval = date2 - date1; 
Console.WriteLine("{0} - {1} = {2}", date2, date1, interval.ToString());
```
## DateTime to String
You can use the ".ToString" function in C# in order to convert DateTime variables to strings.
```csharp
DateTime time = new DateTime();
string time = Convert.ToString(time)
```
## DateTime to Integer
To convert from a DateTime variable to an integer, we can use the C# method of Convert.ToInt32
```csharp
DateTime time = new DateTime();
int time = Convert.ToInt32(time);
```
This may seem counterintuitive to convert to an integer, however this means that you can do arithmetic calculations on your date and time value.
## DateTime Set Using a String, and from Ticks.
To convert ticks to a DateTime variable, you can do this:
```csharp
string dateInput = "Jan 1, 2009"; var parsedDate = DateTime.Parse(dateInput); Console.WriteLine(parsedDate); 
// Displays the following output on a system whose culture is en-US: 
// 1/1/2009 00:00:00
```
Or:

```csharp
DateTime myDate = new DateTime(numberOfTicks);
String test = myDate.ToString("MMMM dd, yyyy");
```
You would convert to a string in order to do things that are exclusive to strings, such as parsing.

