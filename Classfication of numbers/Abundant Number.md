## Implementation

```java[]

import java.util.Scanner;

public class AbundantNumberChecker {
    // Method to calculate the sum of proper divisors
    public static int sumOfDivisors(int n) {
        int sum = 0;
        for (int i = 1; i <= n / 2; i++) {
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

        // Check if the number is Abundant
        if (sumOfDivisors(num) > num) {
            System.out.println(num + " is an Abundant Number.");
        } else {
            System.out.println(num + " is NOT an Abundant Number.");
        }

        scanner.close();
    }
}
````
