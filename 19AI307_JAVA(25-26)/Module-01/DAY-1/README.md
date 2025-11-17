# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
### Write a Java program that:
- Accepts two integer numbers from the user.
- Demonstrates all 5 arithmetic operations:
- Addition (+)
- Subtraction (-)
- Multiplication (*)
- Division (/)
- Modulus (%)
### Displays the result of each operation in a separate line with a clear message.

## AIM:
To write a Java program that accepts two integer numbers from the user and performs all basic arithmetic operations (addition, subtraction, multiplication, division, and modulus), displaying each result clearly.

## ALGORITHM :
1. Start the program.
2. Import the Scanner class and create an object to take user input.
3. Prompt the user to enter two integer numbers.
4. Perform the five arithmetic operations: addition, subtraction, multiplication, division, and modulus.
5. Display the results of each operation with clear messages.
6. End the program.

## PROGRAM:
```
Program to implement variables and Operators using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```
## Sourcecode.java:
```
import java.util.Scanner;
public class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        int num1 = sc.nextInt();
        int num2 = sc.nextInt();

        int sum = num1 + num2;
        int difference = num1 - num2;
        int product = num1 * num2;
        int quotient = num1 / num2;
        int remainder = num1 % num2;

        System.out.println("Sum = " + sum);
        System.out.println("Difference = " + difference);
        System.out.println("Product = " + product);
        System.out.println("Quotient = " + quotient);
        System.out.println("Remainder = " + remainder);
    }
}

```
## OUTPUT:
<img width="471" height="249" alt="image" src="https://github.com/user-attachments/assets/8880815d-01a1-43ff-ad9a-0d936b974deb" />

## RESULT:
Thus, the program is executed successfully, and it correctly performs all five arithmetic operations (addition, subtraction, multiplication, division, and modulus) on the two integers entered.
