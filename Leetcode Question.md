## Largest Consecutive Subsequence

````java[]

import java.util.Arrays;

class Main {
    static int largestConsequence(int[] arr) {
        // Sort the array
        Arrays.sort(arr);

        int lc = 1, count = 1;

        // Find the maximum length by traversing the array
        for (int i = 1; i < arr.length; i++) {
            // Skip duplicates
            if (arr[i] == arr[i - 1])
                continue;

            // Check if the current element is equal to previous element + 1
            if (arr[i] == arr[i - 1] + 1) {
                count++;
            } else {
                // Reset the count
                count = 1;
            }

            // Update the result
            lc = Math.max(lc, count);
        }
        return lc;
    }

    public static void main(String[] args) {
        int[] arr = {2, 6, 1, 9, 4, 5, 3};
        System.out.println("The largest consecutive subsequence length is: " + largestConsequence(arr));
    }
}

````
