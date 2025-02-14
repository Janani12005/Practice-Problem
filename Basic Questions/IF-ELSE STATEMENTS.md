

 ## 01.Positive/Negative 

````java[]

import java.util.*;
public class Main{
    public static void main(String[]args){
        int num = 345;
        if(num>0){
            System.out.println("Positive number");
        }
        else{
            System.out.println("negative number");
        }
    }
}
````

 ## 02.Odd/Even 

````java[]

import java.util.*;
public class Main{
    public static void main(String[]args){
        int num = 357;
        if(num %2 ==0){
            System.out.println("even number");
        }
        else{
            System.out.println("odd number");
        }
    }
    
}
````

## 03. The number is divisible by 3 and 5 

````java[]

import java.util.*;
public class Main {
    public static void main(String[] args) {
        int num = 125;
        if (num % 3 == 0) {
            System.out.println("The number is divisible by 3");
        } else {
            
            System.out.println("The number is divisible by 5");
        }
    }
}
````

## 04. Largest of three numbers 

````java[]

import java.util.*;
public class Main{
    public static void main(String []args){
        int num1 = 34,num2 = 67,num3=90;
        int largest;
        if(num1>=num2 && num1>=num3){
           largest= num1;
        }
           
        else if(num2>=num3 && num1>=num3){
            largest= num2;
        }
        else {
            largest= num3;
        }
          System.out.println("The largest number is:"+ largest);
        }
        
    }
````

## 05.Check whether a number is a prime number 

````java[]

import java.util.*;
public class Main{
    public static void main(String[]args){
        int num = 6453;
        if(num<=2){
            System.out.println("The number is not prime");
        }
        else{
            System.out.println("The number is prime");
        }
    }
    
}
````



