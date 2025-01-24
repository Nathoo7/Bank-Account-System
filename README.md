# Kotlin Bank Account System

## Description
This is a simple **Bank Account System** Android app built using **Kotlin**. The app allows users to deposit and withdraw money from their account, view the transaction history, and track their balance. Below is an explanation of the approach I took for each task.


## Approach for Each Task

### 1. **Prompt the user to enter an initial balance**
* When the app is launched, I prompt the user to enter an initial balance through an EditText field. This field will accept numeric input, which is necessary for the balance.

* To ensure a smooth user experience, a hint is displayed inside the EditText to guide the user on what to enter (e.g., "Enter Initial Balance").

* Once the user enters the balance, the app will validate that the entered value is a valid number and is greater than or equal to zero.

* The entered value will be stored in SharedPreferences into saveBalance(balance: Double) function. 


### 2. **Allow the user to perform deposits and withdrawals**
* To allow deposits and withdrawals, two EditText fields is created, one for entering the deposit amount and one for the withdrawal amount.

* Each field will have an associated button (Deposit Button and Withdraw Button), and when the user clicks either button, the respective amount will be added to or subtracted from the current balance.

* There is input validation to ensure that the user is entering a positive number for deposits and a valid amount for withdrawals by ensuring that the balance is sufficient for the withdrawal.

* The app will then update the balance after each transaction and display the updated balance on the screen.


### 3. **Display the Current Balance After Each Transaction**
* After every deposit or withdrawal, the current balance will be updated and displayed in a TextView.
* The balance will be updated immediately after the transaction is completed, and the TextView will reflect the new balance.
* The displayed balance is formatted properly by showing two decimal places for currency formatting.


## Intsructions

1. BankAccount class is created with methods such as:
* deposit(amount: Double) to handle calculation on adding the amount into balance amount entered by user where the amount entered should be greater than 0;
* withdraw(amount: double) to handle calculation on subtracting of the amount entered by user from the balance amount where the amount entered should be greater than 0 and smaller than or equal to the balance amount;
* getBalance() to retrieve the current balance of the bank account.

2. Implement basic validation
* As shown as in 1. 

3. Provide a main method or main function demonstrating how the class works
* onCreate() method of MainActivity class is the main method as it initializes user interface and set up the logic for handling user interactions.

It handles:

** View Binding Setup:
   -ActivityMainBinding.inflate(layoutInflater) is used to set up the UI using the activity_main.xml layout.

** Initialization:
   -Initializes the BankAccount object.
   -It loads the saved balance and transaction history from SharedPreferences.

** UI Logic:
   -Defines the outcomes when buttons like Submit Balance, Deposit, Withdraw, and View Transaction History are clicked.


## Creativity and extra effort
* This is the xml file in my app:
  -activity_main.xml
  -activity_view_transaction_history.xml (extra)
  -transaction_item.xml (extra, cardView for for listing through recycleView)

*This is the kt file in my app:
 -MainActivity.kt
 -BankAccount.kt
 -ViewTransactionHistoryActivity.kt (extra, responsible for receiving list of transactions )
 -TransactionAdapter.kt (extra, use to display of list in recycleview for transaction histories)
 -Transaction.kt (extra, responsible for data passing by pass list of MainActivity.kt's Transaction object to ViewTransactionHistory.kt and displayed through TransactionAdapter.kt)

* All this created extra files are essential to add View Transaction History page so that user can keep track on how much and what time they deposited and withdrawn from the balance through list of transaction histories.
* SharedPreferences is used to store the simple data so that the balance amount and transaction list will be saved while changing the page.


https://drive.google.com/file/d/1RTtPUCoTdGeU8N79dwb_cR0NiTxVznb2/view?usp=sharing



