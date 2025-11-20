# Ex.No:2(B) METHODS

## QUESTION:
- Create two methods: Get the input for radius from the user.
- double getArea(double r) → calculate the area and return the area(Don't print anything in this method).
- void printArea(double area) → pass the calculated area to this method and print the area of a circle.

## AIM:
To write a Java program that gets the radius of a circle from the user, calculates the area using a method that returns the value, and prints the area using a separate method. 

## ALGORITHM :
1. Start the program.
2. Create a class named prog.
3. Define a method getArea(double r) that:
   - Calculates the area using the formula: area = 3.14 × r × r
   - Returns the calculated area (does not print).
4. Define a method printArea(double area) that:
   - Prints the area using formatted output.
5. In the main() method:
   - Create a Scanner object to read input.
   - Accept radius r from the user.
   - Create an object of the prog class.
   - Call getArea(r) and store the returned value.
   - Call printArea(area) to display the result.
6. End the program.

## PROGRAM:
 ```
Program to implement a Methods using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```
## SOURCE CODE:
```
import java.util.*;
class prog
{
    double getArea(double r)
    {
        return 3.14*r*r;
    }
    void printArea(double area)
    {
        System.out.printf("%.2f",area);
    }
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        double r = sc.nextDouble();
        prog obj = new prog();
        double area = obj.getArea(r);
        obj.printArea(area);
    }
}
```
## OUTPUT:
<img width="368" height="151" alt="image" src="https://github.com/user-attachments/assets/1830c22c-ea21-45f1-a7a6-96fe55d08851" />

## RESULT:
Thus, the program is executed successfully, and the area of the circle is printed based on the radius entered by the user.
