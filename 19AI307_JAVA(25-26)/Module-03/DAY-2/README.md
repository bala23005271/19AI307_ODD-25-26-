# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator 

## AIM:
To write a Java program to calculate the area of different shapes using method overloading in a class AreaCalculator.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class AreaCalculator with overloaded methods named area().
4. Define methods.
5. Create an object of the class and call each method with appropriate arguments.
6. Display the calculated areas and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: bala murugan s
RegisterNumber:  212223230027
*/
```

## SOURCE CODE:


```py
import java.util.Scanner;

public class AreaCalculator {

    // Area of square
    int area(int side) {
        return side * side;
    }

    // Area of rectangle
    int area(int length, int breadth) {
        return length * breadth;
    }

    // Area of circle
    double area(double radius) {
        return Math.PI * radius * radius;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        AreaCalculator ac = new AreaCalculator();

        // Input
        int side = sc.nextInt();          // square
        int length = sc.nextInt();        // rectangle length
        int breadth = sc.nextInt();       // rectangle breadth
        double radius = sc.nextDouble();  // circle

        // Output
        System.out.println("Area of square: " + ac.area(side));
        System.out.println("Area of rectangle: " + ac.area(length, breadth));
        System.out.println("Area of circle: " + ac.area(radius));

        sc.close();
    }
}
```

## OUTPUT:

<img width="918" height="410" alt="image" src="https://github.com/user-attachments/assets/3a484d0d-d506-4fae-b89d-ed20e3244fd2" />



## RESULT:
Thus the program has been implemented and executed successfully.
