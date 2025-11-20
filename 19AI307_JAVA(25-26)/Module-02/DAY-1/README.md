# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class City with attributes: cityName (String), population (long), area (double). Create an object. Print all details.
## AIM:
To create a City class in Java with attributes:
- cityName (String)
- population (long)
- area (double)
Then create an object of the class and print all its details.

## ALGORITHM :
1. Start the program.
2. Create a class named City.
3. Inside the class, declare the attributes:
   - String cityName
   - long population
   - double area
4. Create a constructor to initialize these attributes.
5. In the main() method:
   - Create an object of the City class.
   - Pass appropriate values to the constructor.
6. Print the attributes of the created object.
7. End the program.
   
## PROGRAM:
 ```
Program to implement a Class and Objects using Java
Developed by: Sowmya V
RegisterNumber:  212222110045
```
## SOURCE CODE:
```
import java.util.*;
class city
{
    String city;
    long pop;
    double area;
    
    void printDetails()
    {
        System.out.println("City Name: "+city);
        System.out.println("Population: "+pop);
        System.out.printf("Area: %.1f",area);
    }
}
class prog
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        String city = sc.nextLine();
        long pop = sc.nextLong();
        double area = sc.nextDouble();
        
        city obj = new city();
        obj.city=city;
        obj.pop=pop;
        obj.area=area;
        obj.printDetails();
    }
}
```
## OUTPUT:
<img width="595" height="375" alt="image" src="https://github.com/user-attachments/assets/7d8d86ec-c395-4db9-b874-7848a6b98000" />

## RESULT:
Thus, the program is executed successfully and the details of the city are displayed as expected.
