# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to reverse a number using the Integer wrapper class and compare it with the original number.

## AIM:
To write a Java program that converts a string input into an integer using the Integer wrapper class, reverses the number, and compares it with the original number to check whether it is a palindrome.

## ALGORITHM :
1. Start the program.
2. Read a number as a string using Scanner.
3. Convert the string to an integer using: int num = Integer.parseInt(inp);
4. Store the original number in another variable (og).
5. Initialize a variable rev = 0 to store the reversed number.
6. Use a loop to reverse the number:
   - Extract last digit using num % 10.
   - Multiply rev by 10 and add last digit.
   - Divide num by 10 to remove the last digit.
7. After reversing, compare:
   - If rev == og, the number is a palindrome.
   - Else, print that it is not a palindrome and display the reversed number.
8. End the program.
## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        String inp = sc.next();
        int num = Integer.parseInt(inp);
        int og = num;
        int rev = 0;
        while(num>0)
        {
            rev = rev*10+num%10;
            num/=10;
        }
        if(rev==og)
            System.out.println(og+" is a palindrome number.");
        else
        {
            System.out.println(og+" is not a palindrome number.");
            System.out.println("Reversed Number: "+rev);
        }
    }
}
```
## OUTPUT:

<img width="776" height="259" alt="image" src="https://github.com/user-attachments/assets/0d8e7edb-5c90-4acb-9c1a-91ba94ca212f" />

## RESULT:
The program successfully uses the Integer wrapper class to convert the input string into an integer, reverses the number using arithmetic operations, and correctly determines whether the original number is a palindrome.
