## Implementation

````java[]

import java.util.*;
public class Main {

    // Method to perform left rotation on a string
    public static String leftRotate(String str, int d) {
        if (str == null || str.length() == 0 || d <= 0) {
            return str; // Return the original string if invalid input
        }

        int n = str.length();
        d = d % n; // Ensure d is within the bounds of the string length

        // Concatenate the string with itself
        String concatenated = str + str;

        // Return the substring from index d to d + n
        return concatenated.substring(d, d + n);
    }

    public static void main(String[] args) {
        String str = "abcdef";
        int d = 2; // Number of positions to rotate

        String rotatedStr = leftRotate(str, d);
        System.out.println("Original String: " + str);
        System.out.println("Rotated String: " + rotatedStr);
    }
}

````

             OR


  ````java[]

import java.util.*;
public class Main{
    public static void main(String args[]){
        Scanner s=new Scanner(System.in);
        System.out.print("elements");
        int n=s.nextInt();
        int a[]=new int[n];
        for(int i=0;i<n;i++){
            a[i]=s.nextInt();
        }
        int sum=0;
        System.out.print("Enter the index :");
        int index=s.nextInt();
        for(int i=index;i<a.length;i++){
            sum+=a[i];
        }
        System.out.print("Sum of right elements "+ sum);
    }
}

````
