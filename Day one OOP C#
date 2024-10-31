
using System.ComponentModel;
using System.Drawing;

namespace OOP_1
{
    #region 1. 	Create an enum called "WeekDays" with the days of the week (Monday to Sunday) as its members. Then, write a C# program that prints out all the days of the week using this enum.

    enum WeekDayes
    {
        Monday,
        Tuesday,
        Wednesday,
        Thursday,
        Friday,
        Saturday,
        Sunday
    }

    #endregion


    #region 2.	Define a struct "Person" with properties "Name" and "Age". Create an array of three "Person" objects and populate it with data. Then, write a C# program to display the details of all the persons in the array.

    struct Person
    {
        public int Age { get; set; }

        public string Name { get; set; }

    }

    #endregion


    #region 3.	Create an enum called "Seas on" with the four seasons (Spring, Summer, Autumn, Winter) as its members. Write a C# program that takes a season name as input from the user and displays the corresponding month range for that season. Note range for seasons ( spring march to may , summer june to august , autumn September to November , winter December to February)

    enum Season
    {
        Spring,
        Summer,
        Autumn,
        Winter
    }
    #endregion


    #region 4.	Assign the following Permissions (Read, write, Delete, Execute) in a form of Enum. 	Create Variable from previous Enum to Add and Remove Permission from variable, check if specific Permission is existed inside variable

    [Flags]
    enum Permissions
    {


        Read = 1,
        Write = 2,
        Delete = 4,
        Execute = 7,
    }
    #endregion


    #region 5.	Create an enum called "Colors" with the basic colors (Red, Green, Blue) as its members. Write a C# program that takes a color name as input from the user and displays a message indicating whether the input color is a primary color or not.

    enum Colors
    {
        Red,
        Blue,
        Green

    }
    #endregion


    #region 6.	Create a struct called "Point" to represent a 2D point with properties "X" and "Y". Write a C# program that takes two points as input from the user and calculates the distance between them.
    struct Point
    {
        public double X { get; set; }
        public double Y { get; set; }
    }

    // Method



    #endregion


    #region 7.	Create a struct called "Person" with properties "Name" and "Age". Write a C# program that takes details of 3 persons as input from the user and displays the name and age of the oldest person.



    #endregion

    internal class Program
    {

        #region Question 6 Methods of Struct  X ,Y 
        static Point CreatePoint()
        {
            Point point = new Point();
            Console.WriteLine("X: ");
            point.X = double.Parse(Console.ReadLine());
            Console.WriteLine("Y: ");
            point.Y = double.Parse(Console.ReadLine());
            return point;
        }


        static double DistanceTo(Point p1, Point p2)
        {
            double distance = Math.Sqrt(Math.Pow(p1.X - p2.X, 2) + Math.Pow(p1.Y - p2.Y, 2));
            return distance;
        }
        #endregion

        static void Main(string[] args)
        {
            #region  1.	Create an enum called "WeekDays" with the days of the week (Monday to Sunday) as its members. Then, write a C# program that prints out all the days of the week using this enum.

            foreach (WeekDayes day in Enum.GetValues(typeof(WeekDayes)))
            {
                Console.WriteLine(day);
            }
            #endregion

            #region 2. Define a struct "Person" with properties "Name" and "Age". Create an array of three "Person" objects and populate it with data. Then, write a C# program to display the details of all the persons in the array.

            Person[] Persons = new Person[3];
            Persons[0] = new Person { Name = "Mohamed ", Age = 21 };
            Persons[1] = new Person { Name = "Eid", Age = 61 };
            Persons[2] = new Person { Name = "Wahby", Age = 91 };

            foreach (Person person in Persons)
            {
                Console.WriteLine($"Name : {person.Name} , Age : {person.Age}");

            }

            #endregion

            #region 3.Create an enum called "Seas on" with the four seasons (Spring, Summer, Autumn, Winter) as its members. Write a C# program that takes a season name as input from the user and displays the corresponding month range for that season. Note range for seasons ( spring march to may , summer june to august , autumn September to November , winter December to February)

            Console.WriteLine("Enter a season (Spring,  Summer, Autumn, Winter)");
            if (Enum.TryParse(Console.ReadLine(), true, out Season season))
            {
                switch (season)
                {
                    case Season.Spring:
                        Console.WriteLine("Spring betwen March to May");
                        break;

                    case Season.Summer:
                        Console.WriteLine("Summer betwen June to Agust");
                        break;

                    case Season.Autumn:
                        Console.WriteLine("Autumn Septamper  to Novamber");
                        break;

                    case Season.Winter:
                        Console.WriteLine("Winter betwen Dec to Feb");
                        break;
                    default:
                        Console.WriteLine("Invalid Input ");
                        break;
                }
            }

            #endregion

            #region 4.	Assign the following Permissions (Read, write, Delete, Execute) in a form of Enum. 	Create Variable from previous Enum to Add and Remove Permission from variable, check if specific Permission is existed inside variable
            Permissions permissions = Permissions.Read;

            permissions |= Permissions.Write;
            permissions |= Permissions.Delete;


            Console.WriteLine(permissions);

            permissions &= ~Permissions.Read;
            Console.WriteLine(permissions);

            #endregion

            #region 5.	Create an enum called "Colors" with the basic colors (Red, Green, Blue) as its members. Write a C# program that takes a color name as input from the user and displays a message indicating whether the input color is a primary color or not.

            Console.WriteLine("Enter Your Color: ");
            if (Enum.TryParse(Console.ReadLine(), true, out Colors color))
            {
                if (color == Colors.Red || color == Colors.Green || color == Colors.Blue)

                    Console.WriteLine($"{color} is Primary Color");
                else
                    Console.WriteLine($"{color} is not Primary Color");

            }
            #endregion


            #region 6.	Create a struct called "Point" to represent a 2D point with properties "X" and "Y". Write a C# program that takes two points as input from the user and calculates the distance between them.
            Console.WriteLine("Enter First Point");
            Point p1 = CreatePoint();
            Console.WriteLine("Enter The Scond Point");
            Point p2 = CreatePoint();

            Console.WriteLine($"Distance = {DistanceTo(p1, p2)}");
            #endregion


            #region 7.	Create a struct called "Person" with properties "Name" and "Age". Write a C# program that takes details of 3 persons as input from the user and displays the name and age of the oldest person.

            Person[] persons = new Person[3];
            for (int i = 0; i < 2; i++)
            {
                Console.WriteLine($"Enter the name of person {i+1}");
                string PName = Console.ReadLine();

                Console.WriteLine($"Enter the Age of person {i+1}");
                
                int PAge = int.Parse(Console.ReadLine());

                persons[i] = new Person { Name = PName, Age = PAge };

            }

            Person oldest = persons[0];
            foreach (Person person in persons)
            {
                if (person.Age > oldest.Age)
                    oldest = person;
            }

            Console.WriteLine($"The oldest Person is {oldest.Name} and Age is {oldest.Age}");
        }
            #endregion

    }
}
