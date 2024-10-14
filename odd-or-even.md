using System;

class Program
{
    static void Main()
    {
        // Prompt the user for input
        Console.WriteLine("Enter a number:");
        int number = int.Parse(Console.ReadLine());

        // Check if the number is even or odd
        if (number % 2 == 0)
        {
            Console.WriteLine("The number is even.");
        }
        else
        {
            Console.WriteLine("The number is odd.");   

        }

        // Calculate the factorial of the number
        int factorial = 1;
        for (int i = 1; i <= number; i++)
        {
            factorial *= i;
        }
        Console.WriteLine($"The factorial of {number} is {factorial}.");

        // Check if the number is a prime number
        bool isPrime = true;
        if (number <= 1)
        {
            isPrime = false;
        }
        else
        {
            for (int i = 2; i <= Math.Sqrt(number); i++)
            {
                if (number % i == 0)
                {
                    isPrime = false;
                    break;
                }
            }
        }
        if (isPrime)   

        {
            Console.WriteLine("The number is prime.");
        }
        else
        {
            Console.WriteLine("The number is not prime.");   

        }

        // Find the sum of digits in the number
        int sumOfDigits = 0;
        while (number != 0)
        {
            sumOfDigits += number % 10;
            number /= 10;
        }
        Console.WriteLine($"The sum of digits in {number} is {sumOfDigits}.");
    }
}
