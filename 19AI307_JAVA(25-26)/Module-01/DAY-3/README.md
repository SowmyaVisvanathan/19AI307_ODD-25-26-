# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to reverse a number using a while loop. For example, if the input is 1234, the output should be 4321
## AIM:
To write a Java program that accepts an integer from the user and reverses it using a while loop.

## ALGORITHM :
1. Start the program.
2. Read an integer input from the user.
3. Initialize a variable reversed to 0.
4. Use a while loop to repeat the following steps until the number becomes 0:
   - Extract the last digit using number % 10.
   - Multiply reversed by 10 and add the extracted digit.
   - Remove the last digit from the number using number / 10.
5. After the loop ends, display the reversed number.
6. End the program.

## PROGRAM:
 ```
Program to implement a Looping Statement using Java
Developed by: Sowmya V
Register Number: 212222110045 
```
## SOURCE CODE:
```
import java.util.*;
class prog
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int reversed = 0;
        while (num != 0) 
        {
            int digit = num % 10;
            reversed = reversed * 10 + digit;
            num = num / 10;
        }
        System.out.println("Reversed number: " + reversed);
    }
}

```
## OUTPUT:
<img width="589" height="232" alt="image" src="https://github.com/user-attachments/assets/d99d3023-e893-43c2-b1ed-44d0dbe975f5" />

## RESULT:
Thus, the program successfully reverses the given number using a while loop and displays the reversed number.
