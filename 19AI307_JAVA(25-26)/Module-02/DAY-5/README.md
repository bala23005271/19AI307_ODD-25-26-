# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## AIM:
To create a Java class Calculator with a non-static method add(int a, int b) to return the sum and a static method info() to display a message.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Calculator with a non-static method add(int a, int b) to return the sum of two numbers.
4.	.Define a static method info() that prints "Calculator is ready".
5. Create an object of the class to call the non-static method and use the class name to call the static method.
6. Display the results and stop the program.


## PROGRAM:
 ```

Program to implement a Access Modifiers using Java
Developed by: bala murugan s
RegisterNumber:  212223230027

```

## SOURCE CODE:

```py
import java.util.*;
class Calculator{
    int add(int a, int b){
        return (a+b);
    }
    static void info(){
        System.out.println("Calculator is ready");
    }
    
}
class prog{
    public static void main(String[] args){
        Scanner sc= new Scanner(System.in);
        int a = sc.nextInt();
        int b= sc.nextInt();
        Calculator c= new Calculator();
        c.info();
        System.out.println("Sum: "+c.add(a,b));
    }
}
```

## OUTPUT:

<img width="726" height="281" alt="image" src="https://github.com/user-attachments/assets/6eb6d0b9-687e-4fe0-b74c-507d28fa12e7" />



## RESULT:
Thus the program has been implemented and execued successfully.
