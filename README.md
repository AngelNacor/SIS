# SIS
using System;

class User
{
    
    private string name;
    private string program;
    private string section;
    private string studentNumber;
    private string studentEmail;

    
    public User(string name, string program, string section, string studentNumber, string studentEmail)
    {
        this.name = name;
        this.program = program;
        this.section = section;
        this.studentNumber = studentNumber;
        this.studentEmail = studentEmail;
    }

    
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
        
        User user = new User("Alliah Angel Nacor", "BSIT", "Section 1", "2020-BN-0000", "angelnacor629@gmail.com");

 
        Console.WriteLine("Welcome, " + user.GetName() + "!");
        Console.WriteLine("Please enter a number to choose an option:");
        Console.WriteLine("[1] - See other information");
        Console.WriteLine("[2] - Go Back");

        
        string choice = Console.ReadLine();

        
        switch (choice)
        {
            case "1":
                
                user.DisplayInformation();
                break;
            case "2":
                
                Console.WriteLine("Goodbye!");
                break;
            default:
                Console.WriteLine("Invalid choice.");
                break;
        }
    }
}
