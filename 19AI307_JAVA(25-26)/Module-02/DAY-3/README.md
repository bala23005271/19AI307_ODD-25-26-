# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.


## AIM:

To write a Java program to create a class Smartphone with private variables brand, model, and storageCapacity, provide getter and setter methods, and implement a method to increase storage capacity.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Smartphone with private variables: brand, model, and storageCapacity.
4.	Define public getter and setter methods to access and modify these variables.
5.	Create a method increaseStorage(int value) to add the given value to storageCapacity.
6.	Create an object, set values, call methods, display results, and stop the program.


## PROGRAM:
 ```

Program to implement a Access Specifiers using Java
Developed by: bala murugan s
RegisterNumber: 212223230027

```

## SOURCE CODE:

```py
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    // Getters
    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    // Setters
    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

    // Increase storage
    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }
}

// MAIN CLASS
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Smartphone phone = new Smartphone(); // object created

        phone.setBrand(sc.nextLine());
        phone.setModel(sc.nextLine());
        phone.setStorageCapacity(sc.nextInt());

        int extraStorage = sc.nextInt();
        phone.increaseStorage(extraStorage);

        System.out.println("Brand: "+phone.getBrand());
        System.out.println("Model: "+phone.getModel());
        System.out.println("Updated Storage Capacity: "+phone.getStorageCapacity()+" GB");
        System.out.println("------------------------------");
    }
}

```

## OUTPUT:


<img width="990" height="433" alt="image" src="https://github.com/user-attachments/assets/b8ea2d6d-db2b-4ba0-8506-61cac84f2ccb" />

## RESULT:
Thus the program has been implemented and executed successfully.
