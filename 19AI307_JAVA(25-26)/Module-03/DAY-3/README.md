# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.


## AIM:
To create an abstract class BankAccount with an abstract method calculateInterest() and implement it in subclasses SavingsAccount and FixedDepositAccount.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create an abstract class BankAccount and declare an abstract method calculateInterest().
4.Create a subclass SavingsAccount and override calculateInterest() with its own logic.
5.Create another subclass FixedDepositAccount and override calculateInterest() accordingly.
6.Create objects of both subclasses, call the method, display results, and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: bala murugan s 
RegisterNumber:  212223230027
*/
```

## SOURCE CODE:

```py
import java.util.*;
abstract class BankAccount{
    abstract double calculateInterest();
}
class SavingsAccount extends BankAccount{
    double balance;
    SavingsAccount(double balance){
        this.balance=balance;
    }
    
    double calculateInterest(){
        return balance*0.04;
    }
    
}

class FixedDepositAccount extends BankAccount{
    double amount;
    int years;
    FixedDepositAccount(double amount,int years){
        this.amount=amount;
        this.years=years;
    
    }
    double calculateInterest(){
        return amount*0.07*years;
    }
} 

public class Main{
    public static void main(String[] args){
        Scanner sc= new Scanner(System.in);
        int type=sc.nextInt();
        if(type==1){
            double balance=sc.nextDouble();
            SavingsAccount s=new SavingsAccount(balance);
            System.out.printf("%.2f",s.calculateInterest());
            
        }else if(type==2){
            double amount=sc.nextDouble();
            int years=sc.nextInt();
            FixedDepositAccount f=new FixedDepositAccount(amount,years);
            System.out.printf("%.2f",f.calculateInterest());
        }
    }
}
```




## OUTPUT:

<img width="860" height="401" alt="image" src="https://github.com/user-attachments/assets/d52a36de-1a79-4cba-a1f3-e76c7b630516" />


## RESULT:
Thus the program has been implemented and executed successfully.
