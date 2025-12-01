# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

## AIM:
To write a Java program that takes user input to create multiple Student objects, stores them in an ArrayList, and then serializes (saves) the entire collection into a file and deserializes (reads back) the data from the file.

## ALGORITHM :
1. Start the program.
2. Define a Student class that implements Serializable.
3. Create methods to serialize and deserialize an ArrayList<Student>.
4. Read the number of students from the user.
5. Read each student’s details and store them in an ArrayList.
6. Serialize the ArrayList into a file using ObjectOutputStream.
7. Deserialize the ArrayList from the file using ObjectInputStream.
8. Display the deserialized student data.
9. End the program.
## PROGRAM:
 ```
Program to implement a Serialization and Deserialization using Java
Developed by: Sowmya V
RegisterNumber:  212222110045
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline
        
        // Write your code here
        for(int i=0;i<n;i++)
        {
            int id = scanner.nextInt();
            scanner.nextLine();
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine();
            students.add(new Student(id,name,marks));
        }
        String fn = "students.dat";
        serializeStudents(students,fn);
        List<Student> deserializedStudents = deserializeStudents(fn);
        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}

```
## OUTPUT:
<img width="1172" height="772" alt="image" src="https://github.com/user-attachments/assets/27889319-5f16-4559-8a99-56c0b1cd3754" />

## RESULT:
The program successfully reads multiple student records from the user, stores them in an ArrayList, and serializes the entire collection into a file. It then deserializes the stored data from the file and displays the student details, confirming that the serialization and deserialization processes work correctly.
