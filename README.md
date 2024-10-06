using System;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Enter the first number:");
        string input1 = Console.ReadLine();
        
        Console.WriteLine("Enter the second number:");
        string input2 = Console.ReadLine();

        PerformDivision(input1, input2);
    }

    static void PerformDivision(string num1, string num2)
    {
        try
        {
            // Convert strings to integers
            int dividend = Convert.ToInt32(num1);
            int divisor = Convert.ToInt32(num2);

            // Perform division
            int result = dividend / divisor;

            // Print the result
            Console.WriteLine($"The result of {dividend} divided by {divisor} is: {result}");
        }
        catch (FormatException)
        {
            Console.WriteLine("Error: Please enter valid integers.");
        }
        catch (DivideByZeroException)
        {
            Console.WriteLine("Error: Division by zero is not allowed.");
        }
        catch (Exception ex)
        {
            Console.WriteLine($"An unexpected error occurred: {ex.Message}");
        }
    }
}

