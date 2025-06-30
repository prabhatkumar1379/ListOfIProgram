This File contain List of C# program.
https://www.sanfoundry.com/csharp-programming-examples/
1> W.a.p to get n number of y power.
 2> C# Program to Check Whether a Given Number is Even or Odd
 3>Singleton class ?

 Implementing a Singleton Pattern
The Singleton is a design pattern that restricts the instantiation of a class to a single instance and provides a global point
of access to it. This question will test your understanding of object-oriented programming and design patterns in C#.

Task: Implement a thread-safe Singleton class in C#.

Constraints: The Singleton class should be designed in such a way that only a single instance of the class can exist in the
application, and this instance should be accessible globally.
Explanation:

The Singleton class is defined as sealed to prevent derivation, which could add instances.

A private, read-only padlock object is defined. This is used for thread synchronization to ensure that only one thread can enter the
lock code block at a time. This is important because, without thread safety, two threads could create two separate instances of the 
Singleton class.

The constructor of the Singleton class is defined as private to prevent instantiation from outside the class.

Inside the Instance property, if the Singleton instance is null, a new Singleton object is created and assigned to the instance variable. 
If the Singleton instance already exists, the existing instance is returned.

This question checks your understanding of object-oriented programming, specifically Singleton design pattern. Singleton is one of the 
Gang of Four design patterns and is categorized under creational design patterns as it deals with object creation mechanisms.






# 1.FizzBuzz


```csharp
using System;
namespace CSharpAssesment
{
	public class Program
	{
		public static void Main(string [] args)
		{
			 FizzBuzz(16);
		
		}
		public static void FizzBuzz(int n)
		{
			//TODO: Return "Fizz" if divided by 3, "Buzz" if divided by 5
			//"FizzBuzz" if divided by both, else return the number as a string
			for(int i=1;i<= n; i++)
			{
				if(i % 3 == 0 )
				{
					Console.WriteLine("Fizz");
				}
				else if(i % 5 == 0 )
				{
					Console.WriteLine("Buzz");
				}
				else if(i % 3 ==0 && i % 5 == 0)
				{
					Console.WriteLine("FizzBuzz");
				}
				else
				{
					Console.WriteLine(i);
				}
			}
		
		}
	}
}
 
```
# 2.w.a.p to Reverse string?

```
using System;
using System.Linq; // Required only if you use LINQ-based solution

namespace CSharpAssesment
{
    public class Program
    {
        public static void Main(string[] args)
        {
            string result = ReverseString("Hello World");
            Console.WriteLine(result); // Output: dlroW olleH
        }

        public static string ReverseString(string input)
        {
            // Solution 1 (using LINQ)
            // return new string(input.Reverse().ToArray()); // Simple and readable, requires System.Linq

            //  Solution 2 (without LINQ, using Array.Reverse)
            
            // Step 1: Convert string to character array
            char[] ch = input.ToCharArray();

            // Step 2: Reverse the character array in-place
            Array.Reverse(ch);

            // Step 3: Convert the reversed character array back to string and return
            return new string(ch);
        }
    }
}

```
# 2.1 w.a.p to Reverse string? do't use any built-in reverse method.
```
using System;
namespace CSharpAssesment
{
    public class Program
    {
        public static void Main(string[] args)
        {
            string result = ReverseString("Hello Dev");
            Console.WriteLine(result); // Output: veD olleH
        }

        public static string ReverseString(string input)
        {
		// Create a new character array to hold reversed characters with same size
		char[] reverse = new char[input.Length];
		// Fill the new array with characters from the original string in reverse order
		for( int i =0 ;i<input.Length; i++)
		{
		   reverse[i] =input[input.Length - 1 -i];
		}
		// Convert the reversed character array back to a string and return
		return new string(reverse);
        }
    }
}

```
