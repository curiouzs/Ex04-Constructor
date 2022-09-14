# Ex04-Constructor

## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
 ### Step1:
 Start
 ### Step 2:
 Create a class and a constructor.
 ### Step 3:
 Get name, designation, noofexperience, basic salary and insurance amount from the User.
 ### Step 4:
 Call salary method in constructor to calculate gross salary.
 ### Step 5:
 Call display method to display the output.
 ### Step 6:
 Stop
 
 ## Program:
 ```cs
using System;
namespace RecConst
{
    class Program
    {
        public string name, designation;
        public int noofexperience, basicsalary, insuranceamount;
        float hra, ta, income;
        public Program(string name, string designation, int noofexperience, int basicsalary, int insuranceamount)
        {
            this.name = name;
            this.designation = designation;
            this.noofexperience = noofexperience;
            this.basicsalary = basicsalary;
            this.insuranceamount = insuranceamount;
            salary();
        }
        public void salary()
        {
            hra = (20 / 100) * this.basicsalary;
            ta = (10 / 100) * this.basicsalary;
            income = hra + ta + this.basicsalary - this.insuranceamount;
        }
        public void displayInfo()
        {
            Console.WriteLine("Name of the employee is {0} having {1} of experience, working as {2}", this.name, this.noofexperience, this.designation);
            Console.WriteLine("Receives a salary of {0}", income);

        }
        public static void Main(string[] args)
        {
            Program p1 = new Program("Adhil", "Tester", 10, 30000, 1000);
            Program p2 = new Program("ArunRaj", "Developer", 5, 25000, 1000);
            Program p3 = new Program("Vicki", "Manager", 7, 125000, 5000);
            p1.displayInfo();
            Console.Write("\n");
            p2.displayInfo();
            Console.Write("\n");
            p3.displayInfo();
        }

    }
}
 ```
 
 ## Output:
 ![recc](https://user-images.githubusercontent.com/75234646/190059579-7cb70a53-f7b2-463b-b1da-5ad5ead95344.PNG)

 ## Result:
Thus C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor is executed successfully.
