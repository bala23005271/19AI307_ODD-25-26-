# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Read N numbers from user, use a fixed thread pool (size 3) to compute the sum of each number multiplied by 2. Return results in order.

## AIM:
To write a Java program that reads N numbers from the user, uses a fixed thread pool of size 3 to compute each number multiplied by 2, and returns the results in the same order.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a fixed thread pool of size 3 using Executors.newFixedThreadPool(3).
4. Submit tasks to the thread pool where each task multiplies a number by 2.
5. Store the results using Future objects to maintain the order of input.
6. Retrieve and display the results in order, then shut down the thread pool and end the program.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: bala murugan s 
RegisterNumber: 212223230027
*/
```

## SOURCE CODE:

```py
import java.util.*;
import java.util.concurrent.*;

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);

        int T = sc.nextInt(); // number of tasks

        // Create fixed thread pool of size 3
        ExecutorService executor = Executors.newFixedThreadPool(3);

        List<Future<Integer>> results = new ArrayList<>();

        // Submit tasks
        for (int i = 0; i < T; i++) {
            int num = sc.nextInt();

            Callable<Integer> task = () -> num * 2;

            Future<Integer> future = executor.submit(task);
            results.add(future);
        }

        // Retrieve results in order
        for (Future<Integer> f : results) {
            System.out.println("Result: " + f.get());
        }

        executor.shutdown();
    }
}
```

## OUTPUT:


<img width="956" height="496" alt="image" src="https://github.com/user-attachments/assets/14a4753d-9f7e-4602-ab0a-d95ff67f7059" />



## RESULT:
Thus the program has been implemented and executed successfully.
