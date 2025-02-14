## 01. Check if a number is prime or not using a simple loop

````java[]

import java.util.*;
public class Main{
    public static boolean isPrime(int num){
        if(num <= 1){
        return false;
        
    }
    if(num==2){
        return true;
    }
    for(int i =2;i<=Math.sqrt(num);i++){
        if(num%i==0) {
            return false;
        }
    }
    return true;
    
}
public static void main(String[]args){
   int number =234;
   if(isPrime(number)){
       System.out.println("the number is prime :" + number);
   }
   else{
       System.out.println("the number is not prime :"+ number);
   }
}
}

````

 ## 02. Check if a number is perfect or not

````java[]

import java.util.*;
public class Main {

    public static boolean isPerfectNumber(int num) {
        if (num <= 1) {
            return false; // Numbers less than or equal to 1 are not perfect
        }

        int sum = 0;
        // Find divisors up to half of num
        for (int i = 1; i <= num / 2; i++) {
            if (num % i == 0) {
                sum += i;
            }
        }

        return sum == num; // Return true if sum of divisors equals num
    }

    public static void main(String[] args) {
        int number = 28; 
        if (isPerfectNumber(number)) {
            System.out.println(number + " is a perfect number.");
        } else {
            System.out.println(number + " is not a perfect number.");
        }
    }
}
````
   
