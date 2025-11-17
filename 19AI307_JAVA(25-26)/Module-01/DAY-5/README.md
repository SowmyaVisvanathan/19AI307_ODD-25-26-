# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a java program to check whether a string is a palindrome.

## AIM:

## ALGORITHM :
1. Start the program.
2. Input a string from the user.
3. Convert the string to lowercase to ensure case-insensitive comparison.
4. Initialize an empty string rev to store the reversed string.
5. Use a loop to reverse the string character by character.
6. Compare the original string with the reversed string.
7. If both are equal:
   - Display that the string is a palindrome.
8. Otherwise:
   - Display that the string is not a palindrome.
9. End the program.
## PROGRAM:
```
Program to implement a Strings and Math Function using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```
## SOURCE CODE:
```
import java.util.*;
class prog
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        String str = sc.next();
        String rev = new StringBuilder(str).reverse().toString();
        if(str.equalsIgnoreCase(rev))
            System.out.println(rev+" is a palindrome.");
        else
            System.out.println(str+" is not a palindrome.");
    }
}
```
## OUTPUT:
<img width="723" height="239" alt="image" src="https://github.com/user-attachments/assets/f420f757-d1d1-4d2c-a0e2-8212840e920f" />

## RESULT:
Thus, the program successfully checks whether the given string is a palindrome and displays the appropriate message.

