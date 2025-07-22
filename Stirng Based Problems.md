## 01. Program to count the number of upper-case characters in a given string

````java[]

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
       Scanner sc  =new Scanner(System.in);
       String str = sc.nextLine();
        str= str.replaceAll("[a-z ]","");
        System.out.print(str.length());
        
    }
}
````

## 02. Program to count the special characters in the given string

````java[]

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc  =new Scanner (System.in);
        String str  =sc.nextLine();
        str = str.replaceAll("[a-z0-9]","");
        System.out.print(str.length());
    }
}

````

## 03.  program to find the length of the string without using in-built function

````java[]

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        char[] arr = str.toCharArray();
        int i = 0;
        try{
            for(i=0;;i++){
                char ch = arr[i];
            }
                
            
        }catch(Exception e){
            System.out.print(i);
        }
    }
}

````

## 04. Program to replace all vowels with spaces

````java[]
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
       Scanner sc  = new Scanner(System.in);
        String str = sc.nextLine();
        str = str.replaceAll("['a','e','i','o','u']" ," ");
        System.out.println(str);
    }
}

````

## 05. Program to search for a character in a string

````java[]

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
       Scanner sc  =new Scanner(System.in);
        String str1 = sc.nextLine();
        String str2 = sc.nextLine();
        if(str2.contains(str1)){
            System.out.println("Present");
        }else{
           System.out.println("Not Present");
        }
    }
}

````


## 06.  Program to accept the string and rotate the string n times

````java[]

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        String str = sc.next();
        num = num % str.length();
        String rotated = str.substring(num) + str.substring(0,num);
        System.out.print(rotated);

        
        
        
    }
}

````

## 07. Program to accept the string from the user and display the string in the password format without making any change in the input array

````java[]

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner (System.in);
        String str  = sc.nextLine();
        str = str.replaceAll("[a-zA-Z0-9]","*");
        str = str.replaceAll("[a-zA-Z0-9]","*");
        System.out.println(str);
    }
}
````

## 08. Program to convert the digits of the string into a single number

````java[]

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution{

    public static void Main(
        Scanner sc  =new Scanner(System.in);
       String input = sc.nextLine();

        String result = "";  

        
        for (int i = 0; i < input.length(); i++) {
            char ch = input.charAt(i);
            
            if (ch >= '0' && ch <= '9') {
                result = result + ch;
            }
        }

       
        if (result.equals("")) {
            System.out.println(0);
        } else {
            System.out.println(result);
        }

       
    }
}

````

## 09. Program to reverse a given string without using in-built functions

````java[]

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        StringBuffer str1=new StringBuffer();
        str1.append(str);
        str1 = str1.reverse();
        System.out.println(str1);
        }
            
        
    }

````










