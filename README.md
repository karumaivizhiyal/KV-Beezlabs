# KV-Beezlabs

1) 


2)
class Main {
    static int getMissingNo(int a[], int n)
    {
        int i, total;
        total = (n + 1) * (n + 2) / 2;
        for (i = 0; i < n; i++)
            total -= a[i];
        return total;
    }
    public static void main(String args[])
    {
        int a[] = { 1, 2, 4, 5, 6 };
        int miss = getMissingNo(a, 5);
        System.out.println(miss);
        System.out.println(The missing number from 1 to 8 is);
    }
}


3)
#include <stdio.h>

int main()
{
  int x, y, t;

  printf("Enter two integers\n");
  scanf("%d%d", &x, &y);

  printf("Before Swapping\nFirst integer = %d\nSecond integer = %d\n", x, y);

  t = x;
  x = y;
  y = t;

  printf("After Swapping\nFirst integer = %d\nSecond integer = %d\n", x, y);

  return 0;
}


4)
class GFG 
{ 
static int countDigitOne(int n) 
{ 
    int countr = 0; 
    for (int i = 1; i <= n; i++) 
    { 
        String str = String.valueOf(i); 
        countr += str.split("1", -1) . length - 1; 
    } 
    return countr; 
}  
public static void main(String[] args) 
{ 
    int n = 13; 
    System.out.println(countDigitOne(n)); 
    n = 131; 
    System.out.println(countDigitOne(n)); 
    n = 159; 
    System.out.println(countDigitOne(n)); 
} 
} 


5)
 public int saturdaysundaycount(Date d1, Date d2) {
                Calendar c1 = Calendar.getInstance();
                c1.setTime(d1);
                Calendar c2 = Calendar.getInstance();
                c2.setTime(d2);
                int sundays = 0;
                int saturday = 0;
                while (c1.after(c2)) {
                    if (c2.get(Calendar.DAY_OF_WEEK) == Calendar.SUNDAY || c2.get(Calendar.DAY_OF_WEEK) == Calendar.SUNDAY)
                        sundays++;
                    saturday++;
                    c2.add(Calendar.DATE, 1);
                    c2.add(Calendar.DATE, 1);
                }
                System.out.println(sundays);
                return saturday + sundays;
            }
            
            
6)

import java.io.*;
 
class GFG 
{
    // Function to calculate the angle
    static int calcAngle(double h, double m)
    {
        // validate the input
        if (h <0 || m < 0 || h >12 || m > 60)
            System.out.println("Wrong input");
        if (h == 12)
            h = 0;
             if (m == 60)
       {
        m = 0;
        h += 1;
        if(h>12)
          h = h-12;
        } 
        int hour_angle = (int)(0.5 * (h*60 + m));
        int minute_angle = (int)(6*m);
        int angle = Math.abs(hour_angle - minute_angle);
        angle = Math.min(360-angle, angle);
        return angle;
    } 
    public static void main (String[] args) 
    {
        System.out.println(calcAngle(9, 60)+" degree");
        System.out.println(calcAngle(3, 30)+" degree");
    }
}

 
7)
import java.util.*;
 
class Main{   
    static int digSum(int n)
    {
        int sum = 0;
         while (n > 0 || sum > 9)  
        {
            if (n == 0) {
                n = sum;
                sum = 0;
            }
            sum += n % 10;
            n /= 10;
        }
        return sum;
    }
    public static void main(String argc[])
    {
        int n = 1234;
        System.out.println(digSum(n));
    }
} 


8)
class AverageMarks
{
   public static void main(String args[])
  {
    int i;
    System.out.println("Enter number of subjects");
    Scanner sc=new Scanner(System.in);
    int n=sc.nextInt();
    int[] a=new int[n];
    double avg=0;
    System.out.println("Enter marks");
    for( i=0;i<n;i++)
    {
       a[i]=sc.nextInt();
    }
    for( i=0;i<n;i++)
    {
      avg=avg+a[i];
    }
    System.out.print("Average of (");
    for(i=0;i<n-1;i++)
    {
      System.out.print(a[i]+",");
    }
    System.out.println(a[i]+") ="+avg/n);
  }
}
  



