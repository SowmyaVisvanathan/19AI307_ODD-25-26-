# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

## AIM:
To write a Java program that reads two integers from the user, uses a synchronized block to safely swap their values, and prints the swapped results.

## ALGORITHM :
1. Start the program.
2. Read two integer values a and b from the user.
3. Create a lock object for synchronization.
4. Use a synchronized block to swap the values of a and b.
5. Print the swapped values of a and b.
6. End the program.
   
## PROGRAM:
 ```
Program to implement a Synchronization concept using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```

## SOURCE CODE:
```
import java.util.Scanner;
public class prog
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        Object lock = new Object();
        synchronized (lock) 
        {
            int temp = a;
            a = b;
            b = temp;
        }
        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```
## OUTPUT:
<img width="345" height="297" alt="image" src="https://github.com/user-attachments/assets/f36d0bbe-9818-4283-9c7c-5c98dc44618e" />

## RESULT:
The program successfully accepts two integers, safely swaps their values using a synchronized block, and displays the swapped output.
