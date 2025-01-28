# CodeAlpha_Online_Quiz-_Platform-.
package codealpha2;
import java.util.Scanner;
public class simplebankingsystem {
	public static void main(String[] args) {
		 Scanner scanner = new Scanner(System.in);
	        double balance = 0.0;
	        int choice;

	        do {
	            System.out.println("\nWelcome to Simple Banking Application");
	            System.out.println("1. Deposit");
	            System.out.println("2. Withdraw");
	            System.out.println("3. Check Balance");
	            System.out.println("4. Exit");
	            System.out.print("Enter your choice: ");
	            choice = scanner.nextInt();

	            switch (choice) {
	                case 1:
	                    System.out.print("Enter deposit amount: ");
	                    double depositAmount = scanner.nextDouble();
	                    if (depositAmount > 0) {
	                        balance += depositAmount;
	                        System.out.println("Deposit successful! Current balance: " + balance);
	                    } else {
	                        System.out.println("Invalid amount. Please enter a positive value.");
	                    }
	                    break;

	                case 2:
	                    System.out.print("Enter withdrawal amount: ");
	                    double withdrawAmount = scanner.nextDouble();
	                    if (withdrawAmount > 0 && withdrawAmount <= balance) {
	                        balance -= withdrawAmount;
	                        System.out.println("Withdrawal successful! Current balance: " + balance);
	                    } else if (withdrawAmount > balance) {
	                        System.out.println("Insufficient balance.");
	                    } else {
	                        System.out.println("Invalid amount. Please enter a positive value.");
	                    }
	                    break;

	                case 3:
	                    System.out.println("Your current balance is: " + balance);
	                    break;

	                case 4:
	                    System.out.println("Thank you for using the Simple Banking Application!");
	                    break;

	                default:
	                    System.out.println("Invalid choice. Please try again.");
	            }
	        } while (choice != 4);

	        scanner.close();
	    }
	}
