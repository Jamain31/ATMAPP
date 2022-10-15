# ATMAPP
This program has the same functionality as an ATM machine
In Java, we can create an ATM program for representing ATM transection. In the ATM program, the user has to select an option from the options displayed on the screen. The options are related to withdraw the money, deposit the money, check the balance, and exit.

To withdraw the money, we simply get the withdrawal amount from the user and remove that amount from the total balance and print the successful message.

To deposit the money, we simply get the deposit amount from the user, add it to the total balance and print the successful message.

To check balance, we simply print the total balance of the user.

We use the exit(0) method to exit from the current Transaction mode and return the user to the home page or initial screen.

ATMAPP.java <source code>

package atmApp;

// Import required classes and packages

import java.util.Scanner;

// appATM class to implement the ATM functionality

public class appATM {

// start of main method
	
	public static void main(String[] args) {
		// Variable declaration
		int balance = 1000000, withdraw, deposit;
		
		// Created scanner class object to get choice of user
		
		Scanner sc = new Scanner(System.in);
		
		while(true)
		{
			System.out.println("Automated Teller MAchine");
			System.out.println("Choose 1 for Withdrawl");
			System.out.println("Choose 2 for Deposit");
			System.out.println("Choose 3 for Check BAlance");
			System.out.println("Choose 4 to Exit");
			System.out.println("Choose the operation you want to perform");
			
			//get choice from user
			int choice = sc.nextInt();
			switch(choice)
			{
			case 1:
				System.out.print("Enter money to be withdrawn:");
				
				//Withdrawn money from user
				
				withdraw = sc.nextInt();
				
				// check wether if the balance is greater than or equal to the withdrawn amount
				
				if(balance >= withdraw)
				{
					// remove the withdrawl amount from the total balance
					
					balance = balance -withdraw;
					System.out.println("Please collect your money");
				}
				else
				{
					//show custom error message
					System.out.println("Insufficient Balance");
				}
				System.out.println("");
				break; 
				
			case 2:
				System.out.print("Enter money to be deposited:");
				
				// get deposit amount from user
				
				deposit = sc.nextInt();
				
				// add the deposit amount to the total balance
				
				balance = balance + deposit;
				System.out.println("Your Money has been successfully deposited");
				System.out.println("");
				break;
				
			case 3:
				 //displaying the total balance of the user
				System.out.println("Blance:"+balance);
				System.out.println("");
				break;
				
			case 4:
				//exit from menu
				
				System.exit(0);
				}
			}
		}

	}


![atm-program-java](https://user-images.githubusercontent.com/108758588/195980352-b91a3634-96d6-43c5-a419-91cfd2b7b333.png)
![atm-program-java2](https://user-images.githubusercontent.com/108758588/195980373-fe5a8eae-13c9-4afe-8516-37372a9100e1.png)
