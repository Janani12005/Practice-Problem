## 01.To find the value of pi

````java[]

import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc  =new Scanner(System.in);
	    int num1 = sc.nextInt();
	    int num2 = sc.nextInt();
	    float result = (float)(num1)/num2;
	    
		System.out.printf("%f",result);
	}
}

````

## 02.Conversion of Alphabeic letters small to capital

````java[]

package alphabeticconversion;

import java.util.Scanner;

public class alphabeticconversion {

	public static void main(String[] args) {
		        Scanner sc = new Scanner(System.in);
		        char ch = sc.next().charAt(0);
		        System.out.println((char)(ch ^ 32));
		    }
		


	}
````

## 03.Digit Manipulation

````java[]

package Example1;
import java.util.Scanner;

public class Example1 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
			int n = sc.nextInt();
			int len = (n==0) ? 1:(int) Math.log10(n)+1;
			int place = 1;
			for(int i = 0;i<len-1;i++) {
				place = place*10;
				
		}
			while(place!=0) {
			    System.out.print((n/place)%10);
			    place = place/10;
			}
	}

}
````

## 04.To find the length without using length keyword

````java[]

#include<stdio.h>
int main(){
    char str[100];
    scanf("%s",str);
    int i ;
    for(i =0;str[i];i++);
    printf("%d",i);
    return 0;
}

````

## 05.To find the K-Reverse element

````java[]

package Example1;
import java.util.Scanner;
public class Example1 {
	static int reverse(int n) {
		int rev = 0;
		while(n!=0) {
			rev  =rev*10+(n%10);
			n = n/10;
		}
		return rev;
		
	}

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int n  =sc.nextInt();
		int k =sc.nextInt();
		int t = n;
		int len  =(n==0) ?1:(int)Math.log10(n)+1;
		int place = 1;
		for(int i = 0;i<k;i++) {
			place = place*10;

			}
		int first = n/place;
		int second = n%place;
		System.out.print(first + " "+reverse(second));

	}

}

````

## NUMBER CHRUNCHING

06. To find how many numbers given in the input

````java[]

package Example1;
import java.util.Scanner;
public class Example1 {

	public static void main(String[] args) {
		Scanner sc =new Scanner(System.in);
        int a = sc.nextInt();
        int result  =(a==0)?1:(int)Math.log10(a)+1;
        System.out.println(result);
	}

}
                     (OR)

package Example2;
import java.util.*;

public class Example2 {

	public static void main(String[] args) {
		Scanner sc =new Scanner (System.in);
		int num = sc.nextInt();
		int count = 0;
		while(num>0) {
			num = num/10;
			count = count+1;
		}
		System.out.print(count);
	}

}

````

## 07.Digit Sum 

````java[]

package DigitSum;
import java.util.Scanner;
public class DigitSum {
	static int digitSum(int n) {
		int last,sum = 0;
		while(n>0) {
			last = n%10;
			sum = sum+last;
			n = n/10;
		}
		return sum;
	}

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		while(n>9) {
			n = digitSum(n);
		}
		System.out.println(n);

	}

}
````

## Structural Pattern

1. "W" Pattern:

```` java[]

package structuralpattern1;
import java.util.*;
public class structuralpattern1 {

	public static void main(String[] args) {
		Scanner sc = new Scanner (System.in);
		int num = sc.nextInt();
		for(int row=0;row<num;row++) {
			for(int col = 0;col<num;col++) {
				if(col==0 || col==num-1 ||(row == col &&row>=num/2)|| (row + col==num-1 && row>=num/2)) {
					System.out.print("*");
				}else {
					System.out.print(" ");
				}
			}
			System.out.println();
		}

	}

}

````

2. "Number pattern with odd and even numbers"

````java[]

package structuralpattern2;
import java.util.*;

public class structuralpattern2 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int val = 0;
		for(int row = 0;row<n;row++) {
			val =((row+1)%2==0)?2:1;
			for(int col = 0;col<=row;col++) {
				System.out.print(val);
				val = val+2;
			}
			System.out.println();
			
		}
	}

}
````

3.Alphabetic pattern(12345) model

````java[]
package structuralpattern3;
import java.util.*;
public class structuralpattern3 {

	public static void main(String[] args) {
		Scanner sc = new Scanner (System.in);
		int n = sc.nextInt();
		for(int row = 0;row<n;row++) {
			for(int col = 0 ;col<=row;col++) {
				System.out.print((char)(col+'A'));
			}
			System.out.println();
		}

	}

}
````

4.Number Pattern [1-10 in (12345) model]

````java[]

package structuralpattern4;
import java.util.*;
public class structuralpattern4 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		for(int row = 0;row<n;row++) {
			int val = row+1;
			int diff = n-1;
			for(int col = 0;col<=row;col++) {
				System.out.print(val);
				val = val +diff;
				diff--;
			}
			System.out.println();
		}

	}

}
````

5. "M" Pattern

````java[]

package structuralpattern5;

import java.util.Scanner;

public class structuralpattern5 {

	public static void main(String[] args) {
		Scanner sc = new Scanner (System.in);
		int num = sc.nextInt();
		for(int row=0;row<num;row++) {
			for(int col = 0;col<num;col++) {
				if(col==0 || col==num-1 ||(row == col &&row<=num/2)|| (row + col==num-1 && row<=num/2)) {
					System.out.print("*");
				}else {
					System.out.print(" ");
				}
			}
			System.out.println();
		}
	}

}
````

## 08. Valid Parentheses(Leetcode problem)

````java[]

package Demo1;
import java.util.Scanner;

public class Demo1 {
	public static void main(String[] args) {
		
	
	Scanner sc  =new Scanner(System.in);
	String str = sc.nextLine();
	while(str.contains("()") || str.contains("[]")|| str.contains("{}")) {
		str=str.replace("[]"," ");
		str=str.replace("()"," ");
		str=str.replace("{}"," ");
		
	}
	if(str.length()==0) {
		System.out.print("valid");
		
	}else {
		System.out.print("Invalid");
	}

}
}
````

## 09.Using Character(Parentheses)

````java[]
package usingCharacter;
import java.util.Scanner;
public class usingCharacter {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		char ch  ='e';
		String str = "hello";
		str = "" + ch;
		str = String.valueOf(ch);
		System.out.print(str);

	}

}
````



 








