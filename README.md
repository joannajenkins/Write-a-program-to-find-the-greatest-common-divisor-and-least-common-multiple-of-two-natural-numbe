# Write-a-program-to-find-the-greatest-common-divisor-and-least-common-multiple-of-two-natural-numbe
Write a program to find the greatest common divisor and least common multiple of two natural numbers a and b.
package bai01;
 
import java.util.Scanner;
 
public class Main {
 
    public static int enter()
    {
        Scanner input = new Scanner(System.in);
        boolean check= false;
        int n=0;
        while(!check){
            System.out.print(" ");
            try{
                n= input.nextInt();
                check= true;
            }catch(Exception e){
                System.out.println("You must log in! or log in again...");
                input.nextLine();
            }
        }
        return(n);
    }
    public static int UCLN(int a, int b){
        while(a!= b){
            if(a>b) a= a-b;
            else b= b-a;
        }
        return (a);
    }
    public static void main(String[] args) {
        System.out.println("Speech a");
        int a = enter();
        System.out.println("Tap b");
        int b= enter();
        System.out.println("The common number of "+a+" and "+b+" is: "+UCLN(a,b));
        System.out.println("The most common combination of "+a+" and "+b+" is: "+((a*b)/UCLN(a,b)));
    }
 
}
