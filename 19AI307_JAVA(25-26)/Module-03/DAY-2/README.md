# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:
- area(int side) for square
- area(int length, int breadth) for rectangle
- area(double radius) for circle

## AIM:
To write a Java program that calculates the area of different shapes (square, rectangle, and circle) using method overloading in a class AreaCalculator.

## ALGORITHM :
1. Start the program.
2. Create the class AreaCalculator.
3. Define three overloaded methods:
   - area(int side) → calculates area of a square.
   - area(int length, int breadth) → calculates area of a rectangle.
   - area(double radius) → calculates area of a circle using πr².
4. In the main() method:
   - Create a Scanner object to take user input.
   - side of square
   - length and breadth of rectangle
   - radius of circle
5. Call the corresponding area() methods.
6. Display the area of each shape.
7. End the program.

## PROGRAM:
 ```
Program to implement a Polymorphism using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```

## SOURCE CODE:
```
import java.util.Scanner;
public class AreaCalculator 
{
    void area(int side) 
    {
        int area = side * side;
        System.out.println("Area of square: " + area);
    }

    void area(int length, int breadth) 
    {
        int area = length * breadth;
        System.out.println("Area of rectangle: " + area);
    }

    void area(double radius) 
    {
        double area = Math.PI * radius * radius;
        System.out.println("Area of circle: " + area);
    }

    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        AreaCalculator ac = new AreaCalculator();

        int side = sc.nextInt();
        int length = sc.nextInt();
        int breadth = sc.nextInt();
        double radius = sc.nextDouble();

        ac.area(side);
        ac.area(length, breadth);
        ac.area(radius);

    }
}

```
## OUTPUT:
<img width="830" height="378" alt="image" src="https://github.com/user-attachments/assets/53ddc756-def6-489c-97af-d557ed3d5627" />

## RESULT:
The program successfully demonstrates method overloading by calculating the areas of a square, rectangle, and circle using three area() methods with different parameter lists. It correctly displays the area for each shape based on user input.
