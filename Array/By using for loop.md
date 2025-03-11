##  01. To get an input for size and elements, print the middle element from the array

````java[]
import java.util.Scanner;
public class Main{
 public static void  main(String[] args) {
     Scanner in = new Scanner(System.in);
     int size = in.nextInt();
     int [] marks = new int [size];
     for(int i = 0;i<=size-1;i=i+1){
         marks[i] = in.nextInt();
     }
     int middleIndex = size/2;
     System.out.println("Middle element:" +marks[middleIndex]);
 }

}
````

## 02. Print 2 table by using for loop

````java[]
import java.uttil.*;
public class Main {
    public static void main(String[] args) {
        for (int i = 0; i <= 10; i++) {
            System.out.println(i + "^2 = " + (i * 2));
        }
    }
}
````

## 03.Get input for 5 numbers using array and for loop

````java[]

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int[] marks = new int[5];

        
        for (int i = 0; i < 5; i++) {
            marks[i] = in.nextInt();
        }

        
        for (int i = 0; i < 5; i++) {
            System.out.print(marks[i] + " ");
        }

    }
}
````



