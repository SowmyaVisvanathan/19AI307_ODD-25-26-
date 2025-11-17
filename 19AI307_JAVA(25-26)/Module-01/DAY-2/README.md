# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A pirate ship has a code lock that only opens if:
- The input code is even, and
     - If it is less than 100, say "Weak Code".
     - If it is between 100 and 999, say "Strong Code".
- If the code is odd, deny access.
## AIM:
To write a program that checks a pirate ship's code lock based on the input number and displays whether access is granted or denied according to given conditions.

## ALGORITHM :
1. Start the program.
2. Read the input code from the user.
3. Check if the code is even.
4. If the code is even:
   - If it is less than 100, display "Weak Code".
   - If it is between 100 and 999, display "Strong Code".
5. If the code is odd, display "Access Denied".
6. End the program.

## PROGRAM:
```
Program to implement a conditional statement using Java
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
        int code = sc.nextInt();

        if (code % 2 == 0) 
        {
            if (code < 100) 
                System.out.println("Weak Code");
            else if (code >= 100 && code <= 999) 
                System.out.println("Strong Code");
            else 
                System.out.println("Access Denied");
            
        } 
        else 
            System.out.println("Access Denied");
    }
}

```
## OUTPUT:
<img width="467" height="282" alt="image" src="https://github.com/user-attachments/assets/94b759c3-b5a3-41c0-b067-0a529a633030" />

## RESULT:
Thus, the program successfully checks the pirate ship's code lock and displays whether the code is weak, strong, or access is denied based on the given conditions.
