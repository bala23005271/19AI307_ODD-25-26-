# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.
Note : Read the threadname from the User

## AIM:
To write a Java program that sets the name and priority of the current thread using user input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Get the current thread using Thread.currentThread().
4. Set the thread name using setName() and priority using setPriority().
5. Display the thread name and priority, then end the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: bala murugan s
RegisterNumber: 212223230027
*/
```

## SOURCE CODE:

```py
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read thread name from user
        String threadName = sc.nextLine();

        // Get current thread
        Thread t = Thread.currentThread();

        // Set name and priority
        t.setName(threadName);
        t.setPriority(2);

        // Print details
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
    }
}
```

## OUTPUT:

<img width="1248" height="257" alt="image" src="https://github.com/user-attachments/assets/c23abc42-7e38-4ba1-9ca3-f62116b1bee0" />

## RESULT:
Thus the program has been implemented and executed successfully.
