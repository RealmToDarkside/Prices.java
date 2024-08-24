import java.util.Scanner;

public class PriceAnalyzer {
    public static void main(String[] args) {
        
        Scanner scanner = new Scanner(System.in);
        
       
        double[] prices = new double[20];
        
        
        System.out.println("Enter 20 prices:");
        for (int i = 0; i < prices.length; i++) {
            System.out.print("Price " + (i + 1) + ": $");
            prices[i] = scanner.nextDouble();
        }
        
        
        double sum = 0;
        for (double price : prices) {
            sum += price;
        }
        
        
        System.out.printf("\nSum of all prices: $%.2f%n", sum);
        
        
        System.out.println("\nPrices less than $5.00:");
        for (double price : prices) {
            if (price < 5.00) {
                System.out.printf("$%.2f ", price);
            }
        }
        
        
        double average = sum / prices.length;
        
        System.out.printf("\n\nAverage price: $%.2f%n", average);
        
        System.out.println("\nPrices higher than the average:");
        for (double price : prices) {
            if (price > average) {
                System.out.printf("$%.2f ", price);
            }
        }
        
    }
}
