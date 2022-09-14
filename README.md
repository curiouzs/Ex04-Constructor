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
namespace Exp4
{
    class Employee
    {
        public string name, desig;
        public int exp, bs, ins,gs=0,ta,hra;
        public Employee(string name, string desig, int exp, int bs, int ins)
        {
            this.name = name;
            this.desig = desig;
            this.exp = exp;
            this.bs = bs;
            this.ins = ins;
            salary(bs,ins);
            display(name, desig, exp, gs);
        }
        void salary(int bs,int ins)
        {
            ta = 10*bs/100;
            hra = 20*bs/100;
            gs = bs+ta+hra-ins;
        }
        void display(string name,string desig,int exp,int gs)
        {
            Console.WriteLine("Name of the employee is " + name + " having " + exp + " years of experience,working as " + desig);
            Console.WriteLine("Receives " +gs + " of salary");
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            string name, desig;
            int exp, bs, ins,n;
            Console.WriteLine("Enter no of employees:");
            n=Convert.ToInt32(Console.ReadLine());
            for (int i = 0; i < n; i++)
            {
                Console.WriteLine("Enter the employee name:");
                name = Console.ReadLine();
                Console.WriteLine("Enter the " + name+"'s designation:");
                desig = Console.ReadLine();
                Console.WriteLine("Enter the " + name+"'s experience:");
                exp = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Enter the employee's basic salary:");
                bs = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Enter the "+name+"'s insurance amount:");
                ins = Convert.ToInt32(Console.ReadLine());
                Employee emp = new Employee(name, desig, exp, bs, ins);
            }
            
        }
    }
}
```
 
 ## Output:
 ![Screenshot (186)](https://user-images.githubusercontent.com/75234807/167077088-780c80a8-31b1-44f8-b9ee-c44bb19283fa.png)
 
 ## Result:
Thus C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor is executed successfully.
