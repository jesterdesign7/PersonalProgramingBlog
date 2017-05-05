## https://www.hackerrank.com/challenges/java-currency-formatter

'''java
import java.util.*;
import java.text.*;

public class Solution {
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double payment = scanner.nextDouble();
        scanner.close();
        
        // Write your code here.
        Locale inlocale = new Locale.Builder().setLanguage("en").setRegion("IN").build();
        
        NumberFormat usFormat= NumberFormat.getCurrencyInstance(Locale.US);
       NumberFormat indiaFormat=NumberFormat.getCurrencyInstance(inlocale);
       NumberFormat chinaFormat=NumberFormat.getCurrencyInstance(Locale.CHINA);
       NumberFormat franceFormat=NumberFormat.getCurrencyInstance(Locale.FRANCE);
        
        
        String us= usFormat.format(payment).toString();
        String india= indiaFormat.format(payment).toString();
        String china= chinaFormat.format(payment).toString();
        String france= franceFormat.format(payment).toString();
        
        System.out.println("US: " + us);
        System.out.println("India: " + india);
        System.out.println("China: " + china);
        System.out.println("France: " + france);
    }
}
'''
