# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the index of a given element in an array
## AIM:


## ALGORITHM :
1. Start the program.
2. Declare and initialize an array (or take input from the user).
3. Input the element to be searched.
4. Traverse the array using a loop.
5. Compare each array element with the search element.
6. If a match is found:
   - Display the index.
   - Stop the search.
7. If the element is not found after the loop, display a message saying it is not present.
8. End the program.

## PROGRAM:
```
Program to implement a Array concept using Java
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
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0;i<n;i++)
            arr[i]=sc.nextInt();
        
        int ele=sc.nextInt();
        int ind=-1;
        for(int i=0;i<n;i++)
        {
            if(arr[i]==ele)
            {
                ind=i;
                break;
            }
        }
        if(ind==-1)
            System.out.println("Element not found");
        else
            System.out.println(ind);
    }
}
```
## OUTPUT:
<img width="522" height="496" alt="image" src="https://github.com/user-attachments/assets/17eacc99-ed34-40c5-8dd1-46c0c98dc5b0" />

## RESULT:
Thus, the program successfully finds the index of the specified element in the array and displays it. If the element is not present, it displays an appropriate message.
