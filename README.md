import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the plusMinus function below.
    static void plusMinus(int[] arr) {
        
        int pos=0,neg=0,zero=0;
        float len=arr.length;
        for(int i=0;i<len;i++)
        {
         if(arr[i]>0)
                pos++;
            
            else if(arr[i]<0)
                neg++;

            
            else if(arr[i]==0)
                  zero++;

            if(i==(len-1)){ 

              System.out.printf("%1.6f \n",(pos/len));
              System.out.printf("%1.6f \n",(neg/len));
              System.out.printf("%1.6f \n",(len-(pos+neg))/len);}
        }

    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int n = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        int[] arr = new int[n];

        String[] arrItems = scanner.nextLine().split(" ");
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int i = 0; i < n; i++) {
            int arrItem = Integer.parseInt(arrItems[i]);
            arr[i] = arrItem;
        }

        plusMinus(arr);

        scanner.close();
    }
}
