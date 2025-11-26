# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:
To implement Composition where a Library contains multiple Book objects, and each Book is created inside the Library. Books cannot exist without the Library.

## ALGORITHM :
1. Start
2. Create a Library object.
3. Read the number of books n.
4. Loop n times:
   - Read book title.
   - Read author name.
   - Add a new Book to the Library using library.addBook().
5. After all inputs, call library.showBooks() to display all books.
6. End
   
## PROGRAM:
 ```
Program to implement a Composition Concepts in Java
Developed by: Sowmya V
RegisterNumber: 212222110045
```

## SOURCE CODE:
```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {

    private List<Book> books = new ArrayList<>(); 

    public void addBook(String title, String author) {
        books.add(new Book(title, author));  
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
}

```
## OUTPUT:

<img width="873" height="518" alt="image" src="https://github.com/user-attachments/assets/dab4bea4-f777-4189-a6c8-011e18f50066" />

## RESULT:
The program successfully demonstrates how Composition works by ensuring that Book objects are created and owned entirely by the Library, and cannot exist independently outside it.
