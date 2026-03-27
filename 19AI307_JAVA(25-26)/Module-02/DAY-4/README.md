# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.

## AIM:
To write a Java program to access a static variable using both the class name and an object.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class and declare a static variable inside it.
4.Create an object of the class.
5.Access and display the static variable using the class name and also using the object.

## PROGRAM:
 ```py
/*
Program to implement a Variable scope and Constructor using Java
Developed by:bala murugan s
RegisterNumber:  212223230027
*/
```

## SOURCE CODE:

```py
import java.util.*;

class prog {
    static int num;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        prog.num = sc.nextInt();

        System.out.println("Accessing using class name: " + prog.num);

        prog p = new prog();
        System.out.println("Accessing using object: " + p.num);
    }
}
```

## OUTPUT:

<img width="948" height="337" alt="image" src="https://github.com/user-attachments/assets/57ed318b-92e6-410b-8107-51a743a3c654" />




## RESULT:
Thus the program has been implemented and executed successfully.
