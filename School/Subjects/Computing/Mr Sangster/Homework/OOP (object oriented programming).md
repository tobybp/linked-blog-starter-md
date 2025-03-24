## Namespaces
Namespaces are used to organise code further and prevent variable name conflicts.
Acts as a container for classes and other namespaces.
##### Example:
```csharp
namespace TheNamespace
{
    class TheClass
    {
        public void Message()
        {
            Console.WriteLine("Hello from TheNamespace");
        }
    }
}
```

To use the class TheClass outside of the namespace, you need to do this:

```csharp
using TheNamespace;

class Program
{
    static void Main()
    {
        TheClass obj = new TheClass();
        obj.Message();
    }
}
```
## Classes
A class is a blueprint for creating objects. It defines the parameters (the data) and actions (methods) that objects of the class will have.
##### Declaring a class:
```csharp
class Person
{
    // Properties
    private string name;
    private int age;

    // Constructor
    public Person(string name, int age)
    {
        this.name = name;
        this.age = age;
    }

    // Methods
    public void DisplayInfo()
    {
        Console.WriteLine($"Name: {name}, Age: {age}");
    }
}

```
## Objects
An object is an instance of a class.
You create an object of a class using the `new` keyword.
##### Example (using the class created above):
```csharp
Person joph = new Person("Jophy", 245);
joph.DisplayInfo(); // Output: Name: Jophy, Age: 245
```
## How they are related
- Namespaces group classes together for better organisation.
- Classes define the structure and behaviour of objects.
- Objects are the instances that perform actions and store data as defined by the class.
## Class Global Variables
- Variables defined at the class level are accessible by all methods within the class.
- Static variables are shared across all instances of the class.
- Non-static variables are specific to an individual instance.
##### Example:
```csharp
class Example
{
    // Static variable (shared by all objects)
    public static int sharedCount = 0;

    // Instance variable (unique to each object)
    public int instanceValue;

    public Example(int value)
    {
        instanceValue = value;
        sharedCount++;
    }
}
```
## Static/Non-Static
- Static members belong to the class itself, not to any object. Accessed using the class name. 
- Non-static members belong to individual objects. Accessed through the object.
##### Example:
```csharp
class MathUtility
{
    public static int Add(int a, int b)
    {
        return a + b;
    }
}

class Program
{
    static void Main()
    {
        int sum = MathUtility.Add(5, 3); // Accessing static method
        Console.WriteLine($"Sum: {sum}");
    }
}
```
## Private vs Protected vs Public
- Private - accessible only within the class.
- Protected - accessible within the class and by derived classes.
- Public - accessible from anywhere.
## Declaring a Class
##### Syntax:
```csharp
class ClassName
{
    // Fields, properties, methods, etc.
}
```
##### Example:
```csharp
class Car
{
    public string Make { get; set; }
    public string Model { get; set; }

    public void DisplayCar()
    {
        Console.WriteLine($"Make: {Make}, Model: {Model}");
    }
}
```
## How to Create Objects of Classes
- Use the `new` keyword.
##### Example:
```csharp
Car myCar = new Car();
myCar.Make = "Toyota";
myCar.Model = "Yaris GR";
myCar.DisplayCar();
```
## Accessing Class Public Properties/Methods (from outside the class
- Use the dot `.` operator. 
##### Example:
```csharp
class BankAccount
{
    public string AccountHolder { get; set; }
    public double Balance { get; private set; }

    public void Deposit(double amount)
    {
        Balance += amount;
    }

    public void DisplayAccount()
    {
        Console.WriteLine($"Account Holder: {AccountHolder}, Balance: {Balance}");
    }
}

class Program
{
    static void Main()
    {
        BankAccount account = new BankAccount();
        account.AccountHolder = "Toby BP";
        account.Deposit(999);
        account.DisplayAccount(); // Output: Account Holder: Toby BP, Balance: 999
    }
}
```

## Recap

| Feature            | Desc                                                  |
| ------------------ | ----------------------------------------------------- |
| Namespace          | Organises code and avoids naming conflicts            |
| Class              | Template for creating objects                         |
| Object             | Instance of a class                                   |
| Static Members     | Shared by all objects; accessed using the class name. |
| Non-Static Members | Unique to each object; accessed using the object.     |
| Private            | Accessible only within the class.                     |
| Protected Public   | Accessible within the class and by derived classes.   |
| Public             | Accessible from anywhere                              |
