# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to overwrite the content of a file.

## AIM:

To write a Java program that overwrites the content of a file with new data using FileWriter.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a FileWriter object in overwrite mode (default mode).
4. Write the new content into the file and close the writer.
5. Display a success message and end the program.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: bala murugan s
RegisterNumber: 212223230027
*/
```

## SOURCE CODE:

```py
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class OverwriteFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String content = sc.nextLine(); // read content

        try {
            FileWriter writer = new FileWriter("output.txt"); // overwrite mode
            writer.write(content); // write new content
            writer.close();

            System.out.println("File content overwritten successfully.");
        } catch (IOException e) {
            System.out.println("Error occurred.");
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="1206" height="266" alt="image" src="https://github.com/user-attachments/assets/64e76f2e-5bff-4635-a399-e1aad890acb7" />


## RESULT:
Thus the program has been implemented and executed successfully.

