# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

## AIM:

To write a Java program that serializes a collection of Student objects into a file and then deserializes them back using object streams.

## ALGORITHM :
1.	Start the program
2.	Import the necessary package 'java.util' and read number of students.a
3.	Input student details (id, name, marks) and store them in an ArrayList.
4. Serialize the list using ObjectOutputStream and save it to a file.
5. Deserialize the list using ObjectInputStream from the same file.
6. Display the deserialized student details and end the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: bala murugan s
RegisterNumber:  212223230027
*/
```

## SOURCE CODE:

```py
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

        // Read student details
        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            scanner.nextLine();

            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine();

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        // Serialize
        serializeStudents(students, fileName);

        // Deserialize
        List<Student> deserializedStudents = deserializeStudents(fileName);

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

<img width="1288" height="478" alt="image" src="https://github.com/user-attachments/assets/92e661fa-9c96-48ed-9d85-585403bf39ea" />


## RESULT:

Thus the program has been implemented and executed successfully.
