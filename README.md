# SIS
using System;

class User
{
    // fields
    private string name;
    private string program;
    private string section;
    private string studentNumber;
    private string studentEmail;

    // constructor
    public User(string name, string program, string section, string studentNumber, string studentEmail)
    {
        this.name = name;
        this.program = program;
        this.section = section;
        this.studentNumber = studentNumber;
        this.studentEmail = studentEmail;
    }

    // methods to get user information
    public string GetName()
    {
        return name;
    }

    public string GetProgram()
    {
        return program;
    }

    public string GetSection()
    {
        return section;
    }

    public string GetStudentNumber()
    {
        return studentNumber;
    }

    public string GetStudentEmail()
    {
        return studentEmail;
    }

    // method to display user information
    public void DisplayInformation()
    {
        Console.WriteLine("Name: " + name);
        Console.WriteLine("Program: " + program);
        Console.WriteLine("Section: " + section);
        Console.WriteLine("Student Number: " + studentNumber);
        Console.WriteLine("Student Email: " + studentEmail);
    }
}

class Program
{
    static void Main(string[] args)
    {
        // create a new user object
        User user = new User("Alliah Angel Nacor", "BSIT", "Section 1", "2020-BN-0000", "angelnacor629@gmail.com");

        // display menu options to user
        Console.WriteLine("Welcome, " + user.GetName() + "!");
        Console.WriteLine("Please enter a number to choose an option:");
        Console.WriteLine("[1] - See other information");
        Console.WriteLine("[2] - Go Back");

        // get user's menu choice
        string choice = Console.ReadLine();

        // perform action based on user's choice
        switch (choice)
        {
            case "1":
                // display user's profile information
                user.DisplayInformation();
                break;
            case "2":
                // exit the program
                Console.WriteLine("Goodbye!");
                break;
            default:
                Console.WriteLine("Invalid choice.");
                break;
        }
    }
}
