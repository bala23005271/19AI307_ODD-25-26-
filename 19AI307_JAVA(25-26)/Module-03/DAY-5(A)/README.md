# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To write a Java program to check whether a number is an Armstrong number using Math.pow() and the Integer wrapper class with user input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number from the user using Scanner.
4. Convert the number to Integer (wrapper class) and count the number of digits.
5. Extract each digit, raise it to the power of total digits using Math.pow(), and find the sum.
6. Compare the sum with the original number; if equal, it is an Armstrong number, else not. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: bala murugan  s
RegisterNumber:  212223230027
*/
```

## SOURCE CODE:

```py
import java.util.*;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int num = sc.nextInt();
        int temp = num;
        int sum = 0;

        // using Integer wrapper class
        int digits = Integer.toString(num).length();

        while(temp > 0) {
            int digit = temp % 10;
            sum += Math.pow(digit, digits);
            temp /= 10;
        }

        if(sum == num)
            System.out.println(num + " is an Armstrong number.");
        else
            System.out.println(num + " is not an Armstrong number.");

        sc.close();
    }
}
```

## OUTPUT:

<img width="908" height="258" alt="image" src="https://github.com/user-attachments/assets/ba1ca907-efc6-41f8-8db4-da98ee12d581" />



## RESULT:
Thus the program has been implemented and executed successfully.
