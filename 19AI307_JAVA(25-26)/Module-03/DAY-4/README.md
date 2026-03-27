# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.

## AIM:
To design a Java program where multiple bots analyze weather data by implementing a common interface and provide predictions.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.Create an interface WeatherBot with a method predictWeather().
4. Create multiple classes (bots) that implement the WeatherBot interface.
5. Override the predictWeather() method in each class to give different predictions.
6. Create objects of each bot, call the method, display predictions, and stop the program.	


## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: bala murugan s 
RegisterNumber: 212223230027
*/
```

## SOURCE CODE:

```py
import java.util.*;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if(temperature > 30)
            return "HOT";
        else
            return "MODERATE";
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if(temperature < 20)
            return "COLD";
        else
            return "WARM";
    }
}

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        if(botType == 1) {
            SunBot s = new SunBot();
            System.out.println(s.predict(temperature));
        }
        else if(botType == 2) {
            RainBot r = new RainBot();
            System.out.println(r.predict(temperature));
        }

        sc.close();
    }
}
```




## OUTPUT:

<img width="870" height="260" alt="image" src="https://github.com/user-attachments/assets/f380c134-82ee-40e6-8142-536a2939cd55" />


## RESULT:
Thus the program has been implemented and executed successfully.
