## Bank Account Management
```csharp
using System;

namespace BankingSystem
{
    public class BankAccount
    {
        // Private fields to store account data
        private string accountHolder;
        private double balance;

        // Static variable to track the total number of accounts
        private static int accountCounter = 0;

        // Constructor to initialize the account
        public BankAccount(string holderName, double initialDeposit)
        {
            accountHolder = holderName;
            balance = initialDeposit;
            accountCounter++; // Increment static counter
        }

        // Static method to get the total number of accounts
        public static int GetTotalAccounts()
        {
            return accountCounter;
        }

        // Public method to deposit money
        public void Deposit(double amount)
        {
            if (amount > 0)
            {
                balance += amount;
                Console.WriteLine($"Deposited ${amount}. New balance: ${balance}");
            }
            else
            {
                Console.WriteLine("Deposit amount must be positive.");
            }
        }

        // Public method to withdraw money
        public void Withdraw(double amount)
        {
            if (amount > 0 && amount <= balance)
            {
                balance -= amount;
                Console.WriteLine($"Withdrew ${amount}. New balance: ${balance}");
            }
            else
            {
                Console.WriteLine("Invalid withdrawal amount.");
            }
        }

        // Public method to display account details
        public void DisplayAccountInfo()
        {
            Console.WriteLine($"Account Holder: {accountHolder}, Balance: ${balance}");
        }
    }

    class Program
    {
        static void Main()
        {
            // Create accounts
            BankAccount account1 = new BankAccount("Alice", 1000);
            BankAccount account2 = new BankAccount("Bob", 500);

            // Perform transactions
            account1.Deposit(200);
            account1.Withdraw(100);

            // Display account information
            account1.DisplayAccountInfo();
            account2.DisplayAccountInfo();

            // Show total number of accounts
            Console.WriteLine($"Total Bank Accounts: {BankAccount.GetTotalAccounts()}");
        }
    }
}
```
## Inventory Management System
```csharp
using System;
using System.Collections.Generic;

namespace InventorySystem
{
    public class Product
    {
        // Private fields
        private string name;
        private int stock;
        private double price;

        // Static variable to track total inventory value
        private static double totalInventoryValue = 0;

        // Constructor
        public Product(string name, int stock, double price)
        {
            this.name = name;
            this.stock = stock;
            this.price = price;
            totalInventoryValue += stock * price; // Add to total inventory value
        }

        // Public method to update stock
        public void AddStock(int quantity)
        {
            stock += quantity;
            totalInventoryValue += quantity * price; // Update total inventory value
            Console.WriteLine($"Added {quantity} units to {name}. New stock: {stock}");
        }

        // Public method to sell products
        public void SellProduct(int quantity)
        {
            if (quantity > 0 && quantity <= stock)
            {
                stock -= quantity;
                totalInventoryValue -= quantity * price; // Update total inventory value
                Console.WriteLine($"Sold {quantity} units of {name}. Remaining stock: {stock}");
            }
            else
            {
                Console.WriteLine("Insufficient stock or invalid quantity.");
            }
        }

        // Static method to get total inventory value
        public static double GetTotalInventoryValue()
        {
            return totalInventoryValue;
        }

        // Public method to display product details
        public void DisplayProductInfo()
        {
            Console.WriteLine($"Product: {name}, Stock: {stock}, Price: ${price}");
        }
    }

    class Program
    {
        static void Main()
        {
            // Create product instances
            Product product1 = new Product("Laptop", 10, 800);
            Product product2 = new Product("Phone", 20, 500);

            // Perform operations
            product1.AddStock(5);
            product2.SellProduct(3);

            // Display individual product details
            product1.DisplayProductInfo();
            product2.DisplayProductInfo();

            // Display total inventory value
            Console.WriteLine($"Total Inventory Value: ${Product.GetTotalInventoryValue()}");
        }
    }
}
```
## Library Management System
```csharp
using System;
using System.Collections.Generic;

namespace LibrarySystem
{
    public class Book
    {
        // Private fields
        private string title;
        private string author;
        private bool isBorrowed;

        // Constructor
        public Book(string title, string author)
        {
            this.title = title;
            this.author = author;
            this.isBorrowed = false; // Default to not borrowed
        }

        // Public method to borrow the book
        public void Borrow()
        {
            if (!isBorrowed)
            {
                isBorrowed = true;
                Console.WriteLine($"'{title}' has been borrowed.");
            }
            else
            {
                Console.WriteLine($"'{title}' is already borrowed.");
            }
        }

        // Public method to return the book
        public void Return()
        {
            if (isBorrowed)
            {
                isBorrowed = false;
                Console.WriteLine($"'{title}' has been returned.");
            }
            else
            {
                Console.WriteLine($"'{title}' is not borrowed.");
            }
        }

        // Public method to display book details
        public void DisplayInfo()
        {
            string status = isBorrowed ? "Borrowed" : "Available";
            Console.WriteLine($"Title: {title}, Author: {author}, Status: {status}");
        }
    }

    public class Library
    {
        // List to store books
        private List<Book> books = new List<Book>();

        // Method to add a book to the library
        public void AddBook(Book book)
        {
            books.Add(book);
            Console.WriteLine($"Added '{book.GetType().GetProperty("title")}' to the library.");
        }

        // Method to list all books
        public void ListBooks()
        {
            Console.WriteLine("Library Books:");
            foreach (Book book in books)
            {
                book.DisplayInfo();
            }
        }
    }

    class Program
    {
        static void Main()
        {
            // Create library instance
            Library library = new Library();

            // Add books to the library
            library.AddBook(new Book("1984", "George Orwell"));
            library.AddBook(new Book("To Kill a Mockingbird", "Harper Lee"));

            // List all books
            library.ListBooks();

            // Borrow and return a book
            Book book = new Book("1984", "George Orwell");
            book.Borrow();
            book.DisplayInfo();
            book.Return();
        }
    }
}
```