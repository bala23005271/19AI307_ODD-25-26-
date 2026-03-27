# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

## AIM:
To find the average of the given number using array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	create array
4.	get the input of array
5.	find average and print.


## PROGRAM:
 ```py

Program to implement a Array concept using Java
Developed by: bala murugan s
RegisterNumber:  212223230027

```

## SOURCE CODE:

```py
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a=sc.nextInt();
        int b=0;
        for(int i=0;i<a;i++){
              b+=sc.nextInt();
           

        }
        float f=(float)b/a;
        System.out.printf("The average of elements is %.2f",f);
        }
}
```
## OUTPUT:

<img width="933" height="226" alt="image" src="https://github.com/user-attachments/assets/a51a9315-6791-4a5f-ad09-e55c4dc52a73" />


## RESULT:
Thus , the program to find average has been implemented and executed successfully.
