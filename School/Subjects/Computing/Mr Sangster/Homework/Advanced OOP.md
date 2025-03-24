[[Computing]]
#10/2/25
## Real-Life Entity Explanation

A real-life entity is any object or thing that has properties and methods. Examples include a **Car**, **Person**, or **Bank Account**. In object-oriented programming (OOP), we model real-world entities using **classes and objects**.
### Example:
- **Car**
    - Properties: brand, model, speed
    - Methods: accelerate, brake

---

## Encapsulation Explanation

Encapsulation is the **bundling of data (variables) and methods** that operate on the data into a single unit (a class). It restricts direct access to some of an object's components, enforcing data hiding.
### Example:
- A `BankAccount` class encapsulates the account balance so it **cannot be directly modified**, ensuring security.

---

## Information Hiding Explanation

Information hiding is a principle where **internal details of a class are hidden from the outside** to prevent accidental modifications. It is achieved using **access modifiers** like `private`, `protected`, and `public`.
### Example:
- In a `Car` class, the `engineTemperature` field might be hidden (`private`) so it cannot be changed directly.

---

## Getters and Setters Methods Explanation

Getters and setters allow controlled access to private fields.
- **Getter:** Retrieves a field's value.
- **Setter:** Updates a field’s value while applying constraints.
### C# Example:

```csharp
class Person
{
    private string name;

    public string GetName()  // Getter
    {
        return name;
    }

    public void SetName(string newName)  // Setter
    {
        if (!string.IsNullOrEmpty(newName))
            name = newName;
    }
}
```

---

## Get and Set Keywords

In C#, `get` and `set` are used in **properties** to define accessors.
### Example:

```csharp
class Employee
{
    private int salary;

    public int Salary
    {
        get { return salary; }  // Get keyword
        set { if (value > 0) salary = value; }  // Set keyword
    }
}
```

---

## Inheritance

Inheritance allows a **child class (subclass)** to acquire properties and methods from a **parent class (superclass)**.
- Promotes **code reuse** and **hierarchical classification**.
### Example:
- A `Vehicle` class can be inherited by `Car`, `Truck`, and `Bike`.

---

## Super/Sub Classes

- **Superclass (Parent Class):** The general class that provides properties and methods.
- **Subclass (Child Class):** The specific class that **inherits** from the superclass.
### Example:
- `Animal` (Superclass) → `Dog` (Subclass)

```csharp
class Animal
{
    public void MakeSound()
    {
        Console.WriteLine("Animal makes a sound");
    }
}

class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Dog barks");
    }
}
```

---

## Polymorphism

Polymorphism allows **one interface to be used for different data types**. It can be **compile-time (method overloading)** or **runtime (method overriding)**.

### Example:
- A `Shape` class with a `Draw()` method can be **overridden** in `Circle`, `Rectangle`, and `Square`.

---

## Overriding

Overriding means providing **a new implementation** for a method inherited from a superclass.
### C# Example

```csharp
class Animal
{
    public virtual void Speak()
    {
        Console.WriteLine("Animal speaks");
    }
}

class Dog : Animal
{
    public override void Speak()
    {
        Console.WriteLine("Dog barks");
    }
}
```

---

## Overloading

Overloading occurs when **multiple methods share the same name** but have different **parameters**.
### C# Example

```csharp
class MathOperations
{
    public int Add(int a, int b) => a + b;
    public double Add(double a, double b) => a + b;
}
```

---

## Association

Association represents a **relationship between two independent classes**. There is no ownership.

Example:
- A `Student` and `Course` can exist independently, but a `Student` can enroll in a `Course`.

---

## Aggregation

Aggregation is a **weaker form of association** where one class contains a reference to another, but **both can exist independently**.
### Example:
- A `Library` contains `Books`, but **Books can exist without a Library**.

---

## Composition

Composition is a **stronger form of aggregation**, where one class **owns** another, and the lifecycle of the owned object is dependent on the owner.
### Example:
- A `Car` **has an** `Engine`, and if the `Car` is destroyed, the `Engine` is destroyed too.