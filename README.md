import java.util.Scanner;

public class TipCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the bill amount: ");
        double billAmount = scanner.nextDouble();

        double tipPercentage;
        if (billAmount < 500) {
            tipPercentage = 0.05; // 5%
        } else if (billAmount >= 500 && billAmount <= 1000) { 
tipPercentage = 0.10; // 10%
        } else { // billAmount > 1000
            tipPercentage = 0.15; // 15%
        }

        double tipAmount = billAmount * tipPercentage;
        double totalBillAmount = billAmount + tipAmount;

        System.out.printf("Tip Amount: %.2f Pesos\n", tipAmount);
        System.out.printf("Total Bill Amount: %.2f Pesos\n", totalBillAmount);

        scanner.close();
    }
}
