# Ex.No:3(D)    INTERFACE 

## QUESTION:
Schools use different grading schemes. You need to build a system to plug different strategies.
- SimpleGrader: A: 90+, B: 75–89, C: 60–74, F: below 60
- StrictGrader: A: 95+, B: 85–94, C: 70–84, F: below 70
  
## AIM:
To develop a Java program that implements different grading strategies using interfaces. The program should assign grades based on either a SimpleGrader or StrictGrader strategy, demonstrating polymorphism through interface implementation.

## ALGORITHM :
1. Start the program.
2. Create an interface grader with a method char grade(int marks).
3. Implement class simple:
```
Grading scheme:

A: marks ≥ 90
B: 75–89
C: 60–74
F: below 60
```
4. Implement class strict:
```
Grading scheme:

A: marks ≥ 95
B: 85–94
C: 70–84
F: below 70
```
5. In main():
   - Read student's marks.
   - Read type:
   - 1 → simple grader
   - other → strict grader
6. Create the corresponding grader object.
7. Call g.grade(marks) using interface polymorphism.
8. Print the assigned grade.
9. End program.
   
## PROGRAM:
 ```
Program to implement a Interface using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```
## SOURCE CODE:
```
import java.util.*;
interface grader
{
    char grade(int marks);
}
class simple implements grader
{
    public char grade(int marks)
    {
        if(marks>=90)
            return 'A';
        else if(marks>=75)
            return 'B';
        else if(marks>=60)
            return 'C';
        else 
            return 'F';
    }
}
class strict implements grader
{
    public char grade(int marks)
    {
        if(marks>=95)
            return 'A'; 
        else if(marks>=85)
            return 'B';
        else if(marks>=70)
            return 'C'; 
        else 
            return 'F'; 
    }
}
public class Main
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();
        int type = sc.nextInt();
        grader g;
        if(type==1)
            g=new simple();
        else
            g=new strict();
        System.out.println(g.grade(marks));
    }
}
```
## OUTPUT:
<img width="346" height="151" alt="image" src="https://github.com/user-attachments/assets/7b9abb3d-e251-4d59-9f72-a63580e4b6a7" />

## RESULT:
The program successfully applies different grading strategies based on user choice. It demonstrates polymorphism using the grader interface and dynamically assigns grades according to the SimpleGrader or StrictGrader scheme.
