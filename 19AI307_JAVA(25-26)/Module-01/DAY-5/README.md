# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
Write a Java program to reverse a given string.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.Read the input string from the user.
4.Convert the string into a character array (or access characters using index).
5.Traverse the string from the last character to the first.
6.Print each character in reverse order and stop the program.

## PROGRAM:
 ```py

Program to implement a Strings and Math Function using Java
Developed by: bala murugan s
RegisterNumber: 212223230027

```

## SOURCE CODE:

```py
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner sc= new Scanner(System.in);
        String s= sc.nextLine();
        String r="";
        for(int i=s.length()-1;i>=0;i--){
            r+=s.charAt(i);
        }
        System.out.print("Reversed string: "+r);
        
    }
}

```

## OUTPUT:
Thus, the program has been implemented and executed successfully.



## RESULT:
