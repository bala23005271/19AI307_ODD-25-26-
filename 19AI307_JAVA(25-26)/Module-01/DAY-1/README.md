# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
```
Write a Java program that:

Accepts two integer numbers from the user.

Demonstrates all 5 arithmetic operations:

Addition (+)

Subtraction (-)

Multiplication (*)

Division (/)

Modulus (%)

Displays the result of each operation in a separate line with a clear message.

```


## AIM:


To write a Java program that reads two integer numbers from the user and performs basic arithmetic operations such as addition, subtraction, multiplication, division, and modulus, and displays the results.



## ALGORITHM :
1. Create a Scanner object to read input from the user.
2. Read two values from the user.
3. Compute the following add,sub,mul,div,mod.
4. perform the operations using operator  '+,-,*,/,%'
5. display the results using system.out.println.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: bala murugan s
RegisterNumber: 212223230027
*/
```

## Sourcecode.java:

```
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int a= sc.nextInt();
        int b=sc.nextInt();
        System.out.println("Sum = "+(a+b));
        System.out.println("Difference = "+(a-b));
        System.out.println("Product = "+(a*b));
        System.out.println("Quotient = "+(a/b));
        System.out.println("Remainder = "+(a%b));
    }
}
```

## OUTPUT:

<img width="967" height="366" alt="image" src="https://github.com/user-attachments/assets/24689de1-40d2-411a-9f77-e9f51bdcaeab" />


## RESULT:

The program has been executed successfully and the desired output has been obtained.

