# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java class with a constructor that accepts two numbers as input parameters. The constructor should calculate and display the sum, difference, product, and quotient of the two numbers.

## AIM:
To write a Java program to create a class with a constructor that accepts two numbers as input parameters, calculates the sum, difference, product, and quotient, and displays them.

## ALGORITHM :
1. Start the program.
2. Create a class named cal.
3. Define a constructor in cal that takes two double parameters a and b.
4. Inside the constructor:
   - Calculate the sum, difference, product, and quotient of the two numbers.
   - Print the calculated values using formatted output.
5. Create another class prog with the main() method.
6. In the main method:
   - Create a Scanner object to read input.
   - Accept two numbers from the user.
   - Create an object of cal and pass the input numbers to the constructor.
7. End the program.
   
## PROGRAM:
 ```
Program to implement a Variable scope and Constructor using Java
Developed by: Sowmya V
RegisterNumber:  212222110045
```
## SOURCE CODE:
```
import java.util.*;
class cal
{
    cal(double a, double b)
    {
        double sum = a+b;
        double diff = a-b;
        double mul = a*b;
        double div = a/b;
        
        System.out.printf("Sum: %.1f",sum);
        System.out.printf("\nDifference: %.1f",diff); 
        System.out.printf("\nProduct: %.1f",mul);
        System.out.printf("\nQuotient: %s",div); 
    }
}
class prog
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        double n1=sc.nextDouble();
        double n2=sc.nextDouble();
        cal c1 = new cal(n1,n2);
    }
}
```
## OUTPUT:
<img width="720" height="441" alt="image" src="https://github.com/user-attachments/assets/a838e7e6-d384-4ecb-87b8-db5ff855d982" />

## RESULT:
Thus, the program is executed successfully, and the sum, difference, product, and quotient of the two numbers entered by the user are displayed.
