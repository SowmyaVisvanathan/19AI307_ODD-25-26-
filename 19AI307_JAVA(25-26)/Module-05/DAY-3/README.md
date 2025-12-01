# Ex.No:5(C)  FILE HANDLING USING JAVA

## QUESTION:
Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.

## AIM:
To write a Java program that takes a user’s name, age, and email address as input, and stores this information in a text file (userdata.txt) in a structured format.

## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read user input.
3. Read the name, age, and email from the user.
4. Create a FileWriter to open userdata.txt.
5. Write the collected details into the file in a structured format.
6. Display the same information on the screen.
7. Close the file writer and end the program.
   
## PROGRAM:
 ```
Program to implement a File Handling using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;
class prog
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        try
        {
            String name = sc.next();
            int age = sc.nextInt();
            sc.nextLine();
            String email = sc.nextLine();
            
            FileWriter fw = new FileWriter("userdata.txt");
            fw.write("User Information\n");
            fw.write("================\n");
            fw.write("Name  : "+name+"\n");
            fw.write("Age   : "+age+"\n");
            fw.write("Email : "+email+"\n");
            
            System.out.println("User Information");
            System.out.println("================"); 
            System.out.println("Name  : "+name);
            System.out.println("Age   : "+age); 
            System.out.println("Email : "+email); 
        }
        catch(Exception e)
        {
            
        }
    }
}
```
## OUTPUT:
<img width="679" height="245" alt="image" src="https://github.com/user-attachments/assets/c1d99328-64d9-4eff-81ce-21f93e21faee" />

## RESULT:
The program successfully collects the user's name, age, and email address, writes this data neatly into the file userdata.txt, and displays the information on the console.
