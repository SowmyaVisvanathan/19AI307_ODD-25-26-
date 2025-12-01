# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader 

## AIM:
To write a Java program that reads input from the keyboard using InputStreamReader and BufferedReader, and then displays the entered text.

## ALGORITHM :
1. Start
2. Import required Java I/O classes (java.io.*).
3. Create a class named prog.
4. Inside the main method:
   - Create an object of InputStreamReader to read bytes from the keyboard.
   - Wrap it inside a BufferedReader to read text efficiently.
   - Use readLine() to read a line of input from the user.
   - Store the input in a variable (name).
5. Display the message "Hello, <name>!" to the user.
6. Use a try–catch block to handle exceptions such as I/O errors.
7. End
   
## PROGRAM:
 ```
Program to implement a InputStreamReader using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```

## SOURCE CODE:
```
import java.io.*;
class prog
{
    public static void main(String[] args)
    {
        try
        {
            InputStreamReader isr = new InputStreamReader(System.in);
            BufferedReader br = new BufferedReader(isr);
            String name = br.readLine();
            System.out.println("Hello, "+name+"!");
        }
        catch(Exception e)
        {
            System.out.println("error");
        }
    }
}
```

## OUTPUT:
<img width="438" height="196" alt="image" src="https://github.com/user-attachments/assets/bd11fb24-8766-4dcf-b366-fdf27fc6c332" />

## RESULT:
The program successfully reads a line of text entered by the user from the keyboard and prints a greeting message including the entered text.
