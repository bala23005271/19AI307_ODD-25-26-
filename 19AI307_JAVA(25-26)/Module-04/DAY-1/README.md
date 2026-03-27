# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To identify and prevent NullPointerException while converting strings in an array to uppercase using .toUpperCase().

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create and store input strings in a string array.
4. Traverse the array using a loop.
5. Before calling .toUpperCase(), check if the element is not null.
6. If not null, convert to uppercase and print; otherwise skip. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: bala murugan s 
RegisterNumber:  212223230027
*/
```

## SOURCE CODE:

```py
import java.util.Scanner;

public class UppercaseArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String str = sc.nextLine();

        if (str.equals("null")) {
            System.out.println("Null element");
        } else {
            System.out.println(str.toUpperCase());
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="1083" height="320" alt="image" src="https://github.com/user-attachments/assets/4ad3d85a-7e13-44f9-abdd-c4d0acc5c8f4" />


## RESULT:
Thus the program has been implemented and executed successfully.
