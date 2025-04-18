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

## 03. Find the number is Armstrong or not

````java[]
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input number
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();
        int originalNumber = number;

        // Count digits
        int digits = 0;
        int temp = number;
        while (temp != 0) {
            digits++;
            temp /= 10;
        }

        // Calculate sum of digits raised to power
        int sum = 0;
        temp = number;
        while (temp != 0) {
            int digit = temp % 10;
            sum += Math.pow(digit, digits);
            temp /= 10;
        }

        // Check and display result
        if (sum == originalNumber) {
            System.out.println(originalNumber + " is an Armstrong number.");
        } else {
            System.out.println(originalNumber + " is not an Armstrong number.");
        }

        scanner.close();
    }
}

````

## 04. Calculate the factorial number using recursion

````java[]

import java.util.Scanner;

public class FactorialRecursive {

    // Recursive method to calculate factorial
    static long factorial(int n) {
        if (n == 0 || n == 1)
            return 1;
        else
            return n * factorial(n - 1);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input number
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        // Calculate and print factorial
        long result = factorial(number);
        System.out.println("Factorial of " + number + " is: " + result);

        scanner.close();
    }
}
````
## 05.Check whether the number is Automorphic number

````java[]
import java.util.Scanner;

public class AutomorphicCheck {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input from user
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        if (isAutomorphic(number)) {
            System.out.println(number + " is an Automorphic number.");
        } else {
            System.out.println(number + " is not an Automorphic number.");
        }

        scanner.close();
    }

    // Method to check Automorphic number
    public static boolean isAutomorphic(int num) {
        int square = num * num;

        // Convert both numbers to string
        String numStr = String.valueOf(num);
        String squareStr = String.valueOf(square);

        // Check if square ends with the number
        return squareStr.endsWith(numStr);
    }
}
````

## 06.Find the number is a Fibonacci number

````
import java.util.*;
public class fibonacciseries {
        public static void main(String[] args) {
            int n = 10; // Number of terms to display
            int first = 0, second = 1;

            System.out.println("Fibonacci Series up to " + n + " terms:");

            for (int i = 1; i <= n; i++) {
                System.out.print(first + " ");

                int next = first + second; // Add previous two numbers
                first = second;            // Shift second to first
                second = next;             // Shift next to second
            }
        }
    }

````

## 07.Determine the number is perfect square

````java[]

import java.util.Scanner;
public class perfectsquare {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int num = in.nextInt();
        double sqrt = Math.sqrt(num);
        if(sqrt == (int) sqrt) {
            System.out.println(num + " is a perfect square");
        }
        else{
            System.out.println(" not an perfect square");
        }

    }

}
````

## 08.Count yhe number of digits in a number

````java[]

import java.util.Scanner;
public class perfectsquare {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int num = in.nextInt();
        double sqrt = Math.sqrt(num);
        if(sqrt == (int) sqrt) {
            System.out.println(num + " is a perfect square");
        }
        else{
            System.out.println(" not an perfect square");
        }

    }

}
````

## 09.To check whether  a string is a palindrome

````java[]

public  class palindrome {
    public static void main(String[] args) {
        Scanner in= new Scanner(System.in);
        System.out.println("Enter the string");
        String str = in.nextLine();
        String reversed = "";
        for(int i = str.length()-1;i>=0;i--){
            reversed += str.length();

        }
        if(str.equalsIgnoreCase(reversed)){
            System.out.println("It is a  palindrome");
        }
        else{
            System.out.println("Not a palindrome");
        }
    }
    }
````

## 10.Check if the string is an anagram

````java[]
import java.util.Arrays;
import java.util.Scanner;

public class anagram {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first string: ");
        String str1 = sc.nextLine();

        System.out.print("Enter second string: ");
        String str2 = sc.nextLine();

        // Convert to lowercase and remove spaces
        str1 = str1.replaceAll(" ", "").toLowerCase();
        str2 = str2.replaceAll(" ", "").toLowerCase();

        if (str1.length() != str2.length()) {
            System.out.println("Not anagrams");
        } else {
            char[] ch1 = str1.toCharArray();
            char[] ch2 = str2.toCharArray();

            Arrays.sort(ch1);
            Arrays.sort(ch2);

            if (Arrays.equals(ch1, ch2)) {
                System.out.println("Anagrams");
            } else {
                System.out.println("Not anagrams");
            }
        }

        sc.close();
    }
}
````



   
