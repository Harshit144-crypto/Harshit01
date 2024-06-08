# Harshit01
1.	Print  triangle - and allow user to set height of it in. Like in the following case it’s 4
                                                 
                                                  *
                                                            ***
                                                           *****
                                                          *******

Ans. 
using System;

class Triangle
{
    static void Main()
    {
        Console.WriteLine("Enter the height of the triangle:");
        int height = int.Parse(Console.ReadLine());

        for (int i = 1; i <= height; i++)
        {
            Console.WriteLine(new string(' ', height - i) + new string('*', 2 * i - 1));
        }
    }
}

2.	Find valid date (MMDDYYYY) from string. 

For example :-

 Hdjsh asd2324234jghjsd hjsdg sdhk  12212021 idf32432 32423 d34234jh dfh 

Ans. 
using System;
using System.Text.RegularExpressions;

class ValidDateFinder
{
    static void Main()
    {
        string input = "Hdjsh asd2324234jghjsd hjsdg sdhk 12212021 idf32432 32423 d34234jh dfh";
        string pattern = @"(0[1-9]|1[0-2])(0[1-9]|[12][0-9]|3[01])\d{4}";
        
        MatchCollection matches = Regex.Matches(input, pattern);
        
        Console.WriteLine("Valid dates found:");
        foreach (Match match in matches)
        {
            Console.WriteLine(match.Value);
        }
    }
}
