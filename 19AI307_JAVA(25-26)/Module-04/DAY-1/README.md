# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You have a program that reads an integer from the user. The program must reject any negative number by throwing a special error.How would you design a custom exception to handle this? What message would you display if the user enters a negative number?

## AIM:
To write a Java program that defines and uses a custom exception to handle negative number input. The program should throw a user-defined exception when a negative integer is entered and display an appropriate error message.

## ALGORITHM :
1. Start the program.
2. Create a custom exception class NegEx extending Exception.
   - Pass an error message to the superclass constructor using super().
3. In the main() method:
   - Read an integer n from the user using Scanner.
4. Use a try block to check:
   - If n < 0, throw a new NegEx with the message: "Negative numbers are not allowed"
5. Otherwise, print the valid number.
6. Catch the custom exception using catch (NegEx e) and display the message using e.getMessage().
7. End the program.
## PROGRAM:
 ```
Program to implement a Exception Handling using Java
Developed by: Sowmya V
RegisterNumber: 212222110045 
```

## SOURCE CODE:
```
import java.util.*;
class NegEx extends Exception 
{
    public NegEx(String m) 
    { 
        super(m); 
    }
}
public class prog
{
    public static void main(String[] a) 
    {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        try 
        {
            if (n < 0) 
                throw new NegEx("Negative numbers are not allowed");
            System.out.println("Valid input: " + n);
        } 
        catch (NegEx e) 
        {
            System.out.println(e.getMessage());
        }
    }
}

```
## OUTPUT:

<img width="833" height="289" alt="image" src="https://github.com/user-attachments/assets/d9584659-15ab-4f14-8977-50f6b35fd0ce" />

## RESULT:
The program successfully demonstrates how to design and use a custom exception.
