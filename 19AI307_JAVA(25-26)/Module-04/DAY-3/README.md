# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:
To implement a Java program demonstrating composition, where a Library contains multiple Book objects and books cannot exist independently of the library.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Book with attributes like title and author.
4. Create a class Library that contains a collection (e.g., ArrayList) of Book objects.
5. Inside the Library class, create and manage Book objects (composition).
6. Display the details of all books in the library and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: bala murugan s
RegisterNumber:  212223230027
*/
```

## SOURCE CODE:
```py
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
    private List<Book> books;  // ✅ composition

    public Library() {
        books = new ArrayList<>();
    }

    public void addBook(String title, String author) {
        Book b = new Book(title, author); // ✅ created inside
        books.add(b);
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

<img width="1173" height="592" alt="image" src="https://github.com/user-attachments/assets/d523fbe2-1ad8-4f24-8380-5fddb5872905" />

## RESULT:
Thus the program has been implemented and executed successfully.
