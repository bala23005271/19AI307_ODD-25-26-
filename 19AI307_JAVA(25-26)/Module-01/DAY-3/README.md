# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Write a java program to print fibonacci series.

## AIM:

To write a Java program to generate and print the Fibonacci series up to n terms.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of terms n from the user.Initialize two variables: a = 0 (first term) b = 1 (second term).
4.	Print the first two terms (a and b).
5.	Use a loop from i = 2 to n-1.
6.	Calculate next term: c = a + b .Print c .Update values: a = b ,b = c.
7.	Repeat until n terms are printed.


## PROGRAM:
 ```

Program to implement a Looping Statement using Java
Developed by: bala murugan s
RegisterNumber: 212223230027

```

## SOURCE CODE:

```py
import java.util.Scanner;

public class FibonacciSeries {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int first = 0, second = 1;

        System.out.print("Fibonacci Series: " + first + " " + second);

        for (int i = 3; i <= n; i++) {
            int next = first + second;
            System.out.print(" " + next);
            first = second;
            second = next;
        }

        sc.close();
    }
}


```

## OUTPUT:

<img width="1026" height="274" alt="image" src="https://github.com/user-attachments/assets/8a3a64cc-cf55-4cc3-a430-0ad73453604c" />


## RESULT:
The Java program was executed successfully and the Fibonacci series was generated for the given number of terms.
