## Implementation

````java[]

import java.util.Scanner;

public class NumberTypeChecker {
    // Method to calculate the sum of proper divisors
    public static int sumOfDivisors(int n) {
        int sum = 0;
        for (int i = 1; i <= n / 2; i++) { // Proper divisors are less than N
            if (n % i == 0) {
                sum += i;
            }
        }
        return sum;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Input from user
        System.out.print("Enter a number: ");
        int num = scanner.nextInt();
        
        int sum = sumOfDivisors(num);
        
        // Checking the type of number
        if (sum == num) {
            System.out.println(num + " is a Perfect Number.");
        } else if (sum > num) {
            System.out.println(num + " is an Abundant Number.");
        } else {
            System.out.println(num + " is a Deficient Number.");
        }
        
        scanner.close();
    }
}
````
