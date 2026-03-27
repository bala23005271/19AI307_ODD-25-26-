# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
You are developing a YouTube-like platform. Each channel can have multiple subscribers (viewers). Whenever the channel uploads a new video, it must instantly notify all of its subscribers.

## AIM:
To implement the Observer Design Pattern in Java where a Channel notifies all its Subscribers whenever a new video is uploaded.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface Subscriber with a method update(channelName, videoTitle).
4. Create a class Channel that maintains a list of subscribers and provides methods to subscribe and notify them.
5. When a new video is uploaded, display the upload message and notify all subscribers.
6. Take input for channel name, subscribers, and videos; simulate uploads and display notifications, then stop the program.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: bala murugan s 
RegisterNumber: 212223230027
*/
```

## SOURCE CODE:
```py
import java.util.*;

interface Observer {
    void notify(String channelName, String videoTitle);
}

// Concrete Observer
class Subscriber implements Observer {
    private String name;

    public Subscriber(String name) {
        this.name = name;
    }

    @Override
    public void notify(String channelName, String videoTitle) {
        System.out.println(name + ": New video from " + channelName + "! Watch now...");
    }
}

// Subject
class Channel {
    private String name;
    private List<Observer> subscribers = new ArrayList<>();

    public Channel(String name) {
        this.name = name;
    }

    public void subscribe(Observer subscriber) {
        subscribers.add(subscriber);
    }

    public void uploadVideo(String videoTitle) {
        System.out.println(name + " uploaded: " + videoTitle);
        for (Observer subscriber : subscribers) {
            subscriber.notify(name, videoTitle);
        }
    }
}

// Main program
public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String channelName = sc.nextLine();

        Channel channel = new Channel(channelName);

        int n = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < n; i++) {
            String sub = sc.nextLine();
            channel.subscribe(new Subscriber(sub));
        }

        int v = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < v; i++) {
            String title = sc.nextLine();
            channel.uploadVideo(title);
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="1123" height="329" alt="image" src="https://github.com/user-attachments/assets/8e3ee5ee-0868-4f84-a41d-aec9404c26a6" />

## RESULT:
Thus the program has been implemented and executed successfully.

