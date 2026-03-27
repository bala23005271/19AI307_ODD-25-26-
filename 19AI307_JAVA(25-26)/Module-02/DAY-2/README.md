# Ex.No:2(B) METHODS

## QUESTION:
Write a method int square(int number) that returns the square of a given number.

## AIM:
To write a Java method square(int number) that returns the square of a given number.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Inside the method, calculate the square using number * number.
4.	Return the result to the calling function.
5.	Call the method, display the result, and stop the program.


## PROGRAM:
 ```

Program to implement a Methods using Java
Developed by:bala murugan s  
RegisterNumber:  212223230027

```

## SOURCE CODE:


```py
import java.util.*;
class prog{
    static int square(int number){
        return number*number;
    }
    public static void main(String[] args){
        Scanner sc= new Scanner(System.in);
        int number=sc.nextInt();
        System.out.println(square(number));
    }
}
```




## OUTPUT:

<img width="652" height="185" alt="image" src="https://github.com/user-attachments/assets/de9328a1-bdb0-4ee4-8413-234d1c9a71f3" />


## RESULT:
Thus the program had been implemented and executed successfully.
