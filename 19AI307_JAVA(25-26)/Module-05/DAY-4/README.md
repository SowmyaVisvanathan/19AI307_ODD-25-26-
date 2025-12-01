# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

## AIM:
To write a Java program that sets a new name for the current thread and displays its name and priority.

## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read input from the user.
3. Read the new thread name from the user.
4. Obtain the reference to the current thread using Thread.currentThread().
5. Set the new name to the current thread.
6. Display the priority of the current thread.
7. Display the name of the current thread.
8. Display the thread information using toString().
9. End the program.
    
## PROGRAM:
 ```
Program to implement a Thread Priority Concept using Java
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

        String newName = sc.nextLine();
        Thread t = Thread.currentThread();
        t.setName(newName);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
    }
}

```
## OUTPUT:
<img width="686" height="197" alt="image" src="https://github.com/user-attachments/assets/5a280089-a558-4377-960c-53a7b92f4098" />

## RESULT:
The program successfully reads a new name for the current thread, updates the thread's name, retrieves its priority, and displays both the priority and the updated name along with complete thread information.
