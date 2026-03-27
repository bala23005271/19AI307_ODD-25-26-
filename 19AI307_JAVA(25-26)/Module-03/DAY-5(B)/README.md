# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is prime using wrapper classes. 

## AIM:

To write a Java program to check whether a given number is a prime number using wrapper classes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number from the user and convert it into an Integer object (wrapper class).
4. Check if the number is less than or equal to 1 (not prime).
5. Use a loop from 2 to n/2 (or √n) to check divisibility.
6. If divisible, it is not prime; otherwise, it is prime. Display the result and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: bala murugan s
RegisterNumber: 212223230027
*/
```

## SOURCE CODE:

```py
import java.util.Scanner;

public class PrimeWrapper {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Integer num = Integer.valueOf(sc.nextLine());
        boolean isPrime = true;

        if (num <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i <= num / 2; i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        if (isPrime) {
            System.out.println(num + " is a prime number.");
        } else {
            System.out.println(num + " is not a prime number.");
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="865" height="280" alt="image" src="https://github.com/user-attachments/assets/4f19cada-4864-4f3a-8680-aef48e9e114a" />


## RESULT:
Thus the program has been implemented and executed successfully.
