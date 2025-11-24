# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program that demonstrates the use of a non-static inner class.
The outer class should accept a name, and the inner class should display a greeting message using that name.

## AIM:
To create a Java program that uses an inner class to access and display data from its outer class, demonstrating the concept of inner classes in Java.

## ALGORITHM :
1. Start the program.
2. Define the class OuterClass with:
   - A data member name.
   - A constructor to initialize the name.
   - A method display() that creates an object of the inner class and calls its method.
3. Define an InnerClass inside OuterClass with:
   - A method showMessage() that prints a greeting using the outer class variable name.
4. In the main() method:
   - Create a Scanner object to read a string input from the user.
   - Create an object of OuterClass using the input.
   - Call the display() method to show the message from the inner class.
5. End the program.
   
## PROGRAM:
 ```
Program to implement a InnerClass using Java
Developed by: Sowmya V
RegisterNumber: 212222110045 
```

## SOURCE CODE:
```
import java.util.Scanner;

class OuterClass {
    String name;

    OuterClass(String name) {
        this.name = name;
    }

    void display() {
        InnerClass inner = new InnerClass();
        inner.showMessage();
    }

    class InnerClass {
        void showMessage() {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("");
        String input = scanner.next();
        scanner.close();

        OuterClass outer = new OuterClass(input);
        outer.display();
    }
}
```
## OUTPUT:

![WhatsApp Image 2025-11-24 at 13 53 36_7a73581d](https://github.com/user-attachments/assets/d7cee3e0-4df9-48c3-affb-c329e36748c0)

## RESULT:
The program successfully demonstrates the concept of inner classes.
