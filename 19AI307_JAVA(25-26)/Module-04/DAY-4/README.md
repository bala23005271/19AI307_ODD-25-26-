# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Simulate a fan speed controller using the State Pattern. Each time the user types "next", change fan speed from Off -> Low -> Medium -> High -> Off.


## AIM:
To implement a Fan Speed Controller using the State Design Pattern, where the fan cycles through states: Off → Low → Medium → High → Off when the user enters "next".

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a State interface with a method next(Fan fan).
4. Implement concrete states: OffState, LowState, MediumState, and HighState, each defining the next state.
5. Create a Fan class that maintains the current state and changes state when "next" is entered.
6. Take user input repeatedly, update state, display fan speed, and stop when "exit" is entered.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: bala murugan s 
RegisterNumber: 212223230027
*/
```

## SOURCE CODE:
```py
import java.util.Scanner;

interface FanState {
    FanState next();
}

class OffState implements FanState {
    public FanState next() {
        System.out.println("Fan is on Low");
        return new LowState();
    }
}

class LowState implements FanState {
    public FanState next() {
        System.out.println("Fan is on Medium");
        return new MediumState();
    }
}

class MediumState implements FanState {
    public FanState next() {
        System.out.println("Fan is on High");
        return new HighState();
    }
}

class HighState implements FanState {
    public FanState next() {
        System.out.println("Fan is Off");
        return new OffState();
    }
}

class Fan {
    private FanState state = new OffState();

    public void next() {
        state = state.next();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Fan fan = new Fan();

        while (true) {
            String input = sc.nextLine();
            if (input.equalsIgnoreCase("exit")) break;

            if (input.equalsIgnoreCase("next")) {
                fan.next();
            }
        }
    }
}
```

## OUTPUT:

<img width="943" height="413" alt="image" src="https://github.com/user-attachments/assets/64204337-c037-49bf-b82a-30892cffc34c" />


## RESULT:

Thus the program has been implemented and executed successfully.
