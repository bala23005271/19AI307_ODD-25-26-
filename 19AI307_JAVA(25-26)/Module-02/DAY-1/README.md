# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To create a Java class Car with attributes brand, model, and year, create two objects, and print their details.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class Car with attributes: brand, model, and year.
4.	Create two objects of the Car class and assign values to their attributes.
5.	Access and print the details of both objects using System.out.println().


## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: bala murugan s 
RegisterNumber:  212223230027
*/
```

## SOURCE CODE:


```py
class Car{
    String brand;
    String model;
    int year;
}
public class prog {
    public static void main(String[] args) {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}
```




## OUTPUT:

<img width="883" height="205" alt="image" src="https://github.com/user-attachments/assets/3f1ad544-45ce-43e8-b483-2f4a5bf24868" />



## RESULT:
Thus the program has been executed and implemented successfully.
