# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:

## AIM:
To create a superclass Person with fields name and age, and a subclass Student that adds marks and includes a method calculateGrade() to determine the grade based on marks.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a superclass Person with variables name and age.
4. Create a subclass Student that inherits from Person and adds a variable marks.
5. Implement a method calculateGrade() in Student to return grade based on marks (using conditions).
6. Create an object, assign values, display details and grade, then stop the program.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: bala murugan s
RegisterNumber:  212223230027
*/
```

## SOURCE CODE:

```py
import java.util.Scanner;

// Superclass
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

// Subclass
class Student extends Person {
    int marks;

    Student(String name, int age, int marks) {
        super(name, age);   // call superclass constructor
        this.marks = marks;
    }

    char calculateGrade() {
        if (marks >= 90) {
            return 'A';
        } else if (marks >= 75) {
            return 'B';
        } else if (marks >= 50) {
            return 'C';
        } else {
            return 'F';
        }
    }
}

// Main class
public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Getting input from user
    
        String name = sc.nextLine();

        
        int age = sc.nextInt();

        
        int marks = sc.nextInt();

        // Creating object
        Student s = new Student(name, age, marks);

        // Display output
        
        System.out.println("Name: " + s.name);
        System.out.println("Age: " + s.age);
        System.out.println("Marks: " + s.marks);
        System.out.println("Grade: " + s.calculateGrade());

        sc.close();
    }
}

```

## OUTPUT:
<img width="870" height="297" alt="image" src="https://github.com/user-attachments/assets/c0bbaa66-d0fe-4765-9873-5b92f560aaf3" />



## RESULT:
Thus the program has been implemented and executed successfully.
