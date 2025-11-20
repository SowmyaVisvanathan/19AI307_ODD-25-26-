# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program that defines a class Person with private variables:
- name (String)
- age (int)
- country (String)
The program should provide public getter and setter methods to access and modify these private variables. In the main method, take user input and display the details using getters.

## ALGORITHM :
1. Start the program.
2. Create a class named Person.
3. Declare the instance variables name, age, and country as private so they cannot be accessed directly from outside the class.
4. Create public setter methods:
   - setName(String name) — assigns value to the name variable.
   - setAge(int age) — assigns value to the age variable.
   - setCountry(String country) — assigns value to the country variable.
5. Create public getter methods:
   - getName() — returns the name.
   - getAge() — returns the age.
   - getCountry() — returns the country.
6. In the main() method:
   - Create a Scanner object to read input from the user.
   - Create a Person object.
   - Use setter methods to store user-entered values.
   - Use getter methods to print the stored values.
7. End the program.
## PROGRAM:
 ```
Program to implement a Access Specifiers using Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```

## SOURCE CODE:
```
import java.util.*;
public class Person 
{
    private String name;
    private int age;
    private String country;
    
     public String getName() 
     {
         return name; 
     }
     public void setName(String name) 
     {
         this.name = name; 
     }
     public int getAge() 
     {
         return age; 
     }
     public void setAge(int age)
     {
         this.age = age; 
     }
     public String getCountry() 
     {
         return country;
     } 
     public void setCountry(String country) 
     {
         this.country = country; 
     }
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        Person p = new Person();
        
        p.setName(sc.next());
        p.setAge(sc.nextInt());
        p.setCountry(sc.next());
        
        System.out.println("Person 1");
        System.out.println("Name: "+p.getName());
        System.out.println("Age: "+p.getAge());
        System.out.println("Country: "+p.getCountry());
    }
}

```
## OUTPUT:
<img width="710" height="399" alt="image" src="https://github.com/user-attachments/assets/89848e5a-182d-4de8-b233-4ec63ed290a9" />

## RESULT:
Thus, the program is executed successfully, and the details of the person (name, age, and country) are displayed based on the values entered by the user.
