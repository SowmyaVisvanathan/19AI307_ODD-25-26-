# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".
## AIM:
To write a Java program to create a class Calculator with a non-static method add(int a, int b) that returns the sum of two numbers, and a static method info() that displays the message "Calculator is ready".

## ALGORITHM :
1. Start the program.
2. Create a class named Calculator.
3. Inside the class:
   - Define a non-static method add(int a, int b) that returns the sum of a and b.
   - Define a static method info() that prints the message "Calculator is ready".
4. In the main method:
   - Call the static method info().
   - Create an object of Calculator.
   - Call the add() method and print the returned sum.
5. End the program.
## PROGRAM:
 ```
Program to implement a Access Modifiers using Java
Developed by: Sowmya V
RegisterNumber:  212222110045
```

## SOURCE CODE:
```
import java.util.Scanner;
class Calculator 
{
    void info()
    {
        System.out.println("Calculator is ready");
    }
    int add(int a, int b)
    {
        return a+b;
    }
}
class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        Calculator c = new Calculator();
        c.info();
        System.out.println("Sum: "+c.add(a,b));
    }
}

```
## OUTPUT:
<img width="544" height="301" alt="image" src="https://github.com/user-attachments/assets/31c2f547-6bbb-43f8-aa34-6957afd88554" />

## RESULT:
Thus, the program is executed successfully, and the message “Calculator is ready” is displayed, followed by the sum returned by the add() method.
