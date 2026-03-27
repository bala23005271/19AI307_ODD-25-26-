# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
To write a Java program that takes a file name and content as input and writes the content into the specified file using FileWriter.

## ALGORITHM :
1.	Start the program.
2. Read the file name and content from the user using Scanner.
3. Create a FileWriter object with the given file name.
4. Write the content into the file using the write() method and close the file.
5. Display a success message and end the program..	

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: bala murugan s
RegisterNumber: 212223230027
*/
```

## SOURCE CODE:

```py
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class WriteFileUsingFileWriter {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String fileName = sc.nextLine();   // read file name
        String content = sc.nextLine();    // read content

        try {
            FileWriter writer = new FileWriter(fileName); // create file
            writer.write(content); // write content
            writer.close(); // close writer

            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="998" height="358" alt="image" src="https://github.com/user-attachments/assets/7776414f-daf7-488b-833c-9be3c2e8f85c" />

## RESULT:

Thus the program has been implemented and executed successfully.
