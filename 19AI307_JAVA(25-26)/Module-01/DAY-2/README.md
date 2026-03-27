# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

In a haunted house, lights turn on or off based on the hour of entry:
If the hour is even and between 2 and 6 (inclusive), lights flicker.If the hour is odd and between 7 and 11, lights stay off.If the hour is 12, lights turn red.
Otherwise, the house is dark.

Input	Result

4           Lights flicker


## AIM:
To write a program and print the result using conditional statements.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Get the input from te user.
4.	use the conditional statements i.e, if,else-if and else.
5.	check which condition satisfy the input and print.

## PROGRAM:
 ```py

Program to implement a conditional statement using Java
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
        if(a%2==0){
            if(a>2 && a<=6){
                System.out.println("Lights flicker");
            }else if(a==12){
                System.out.println("Lights red");
            }
            
        }else if(a==7){
            System.out.println("Lights off");
        }
        else{
            System.out.println("Dark house");
        }
}
}
```

## OUTPUT:

<img width="1294" height="320" alt="image" src="https://github.com/user-attachments/assets/9effb7e0-22eb-4272-9f42-c96099c5f50a" />


## RESULT:

Thus the program has been implemented and executed successfully using conditional statement .
