## Implementation

````java[]

import java.util.*;
public class Main{
    public static void main(String[]args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int index=sc.nextInt();
        int arr[]=new int[n];
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        int sum=sumright(arr,index);
        System.out.print(sum);
    }
       
    public static int sumright(int arr[],int index){
        int sum=0;
        for(int i=index+1;i<arr.length;i++){
            sum+=arr[i];
        }
        return sum;
    }
       
       
}

````
