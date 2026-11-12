# a




using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    class Program
    {
        public static void addition(double a, double b)
        {
            double c = a + b;
            Console.WriteLine("The answer is : " + c);
        }

        public static void subtraction(double a, double b)
        {
            double c = a - b;
            Console.WriteLine("The answer is : " + c);
        }

        public static void multiplication(double a, double b)
        {
            double c = a * b;
            Console.WriteLine("The answer is : " + c);
        }

        public static void division(double a, double b)
        {
            double c = a / b;
            Console.WriteLine("The answer is : " + c);
        }



        static void Main(string[] args)
        {
            int x = 0;
            try
            {
                do
                {

                    Console.WriteLine("Enter first number");
                    double a = Convert.ToDouble(Console.ReadLine());

                    Console.WriteLine("Enter operator = + - * /");
                    string ope = Console.ReadLine();

                    if (ope != "+" && ope != "-" && ope != "*" && ope != "/")
                    {
                        Console.WriteLine("please enter a proper operator");
                        return;
                    }

                    Console.WriteLine("Enter second number");
                    double b = Convert.ToDouble(Console.ReadLine());

                    if (ope == "+")
                    {

                        addition(a, b);

                    }
                    else if (ope == "-")
                    {

                        subtraction(a, b);

                    }
                    else if (ope == "*")
                    {

                        multiplication(a, b);

                    }
                    else if (ope == "/")
                    {

                        division(a, b);

                    }

                    Console.WriteLine("Do you want to calculate again? yes or no");

                    string ans = Console.ReadLine();

                    if (ans.ToLower() == "yes")
                    {

                    } else if (ans.ToLower() == "no")
                    {

                        x++;

                    } else
                    {
                        Console.WriteLine("Enter a proper answer next time, now repeating");
                    }

                } while (x == 0);

            } catch (Exception e)
            {
                Console.WriteLine("Please put a proper number and operator :)");
            }
            

        }
    }
}
