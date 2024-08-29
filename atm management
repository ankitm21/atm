#include <iostream>
#include <cstdlib>
#include <string>
using namespace std;

class Bank {
private:
    string customerName;
    long long accountNumber;
    char accountType[10];
    long long balance = 0;
    long long depositAmount = 0;

public:
    // Function to initialize account details
    void initializeAccount() {
        cout << "Enter Customer Name: ";
        cin.ignore();  // Clears the input buffer
        getline(cin, customerName);

        cout << "Enter Account Number: ";
        cin >> accountNumber;

        cout << "Enter Account Type (Savings/Current): ";
        cin >> accountType;

        cout << "Enter Initial Balance: ";
        cin >> balance;
    }

    // Function to display account details
    void displayAccountDetails() {
        cout << "\nCustomer Name: " << customerName << endl;
        cout << "Account Number: " << accountNumber << endl;
        cout << "Account Type: " << accountType << endl;
        cout << "Current Balance: " << balance << endl;
    }

    // Function to deposit money into the account
    void depositMoney() {
        cout << "\nEnter Amount to Deposit: ";
        cin >> depositAmount;
        balance += depositAmount;
    }

    // Function to display balance
    void displayBalance() {
        cout << "\nTotal Balance: " << balance << endl;
    }

    // Function to withdraw money from the account
    void withdrawMoney() {
        long long withdrawalAmount;
        cout << "\nEnter Amount to Withdraw: ";
        cin >> withdrawalAmount;

        if (withdrawalAmount > balance) {
            cout << "Insufficient funds! Cannot proceed with the withdrawal." << endl;
        } else {
            balance -= withdrawalAmount;
            cout << "Withdrawal successful!" << endl;
        }
    }
};

int main() {
    Bank myBank;
    int option;

    while (true) {
        cout << "\n============ ATM Management System ============" << endl;
        cout << "1. Initialize Account" << endl;
        cout << "2. View Account Details" << endl;
        cout << "3. Deposit Money" << endl;
        cout << "4. Check Balance" << endl;
        cout << "5. Withdraw Money" << endl;
        cout << "6. Exit" << endl;
        cout << "Choose an option: ";
        cin >> option;

        switch (option) {
            case 1:
                myBank.initializeAccount();
                break;
            case 2:
                myBank.displayAccountDetails();
                break;
            case 3:
                myBank.depositMoney();
                break;
            case 4:
                myBank.displayBalance();
                break;
            case 5:
                myBank.withdrawMoney();
                break;
            case 6:
                cout << "Exiting the system. Thank you!" << endl;
                exit(0);
            default:
                cout << "Invalid option! Please try again." << endl;
        }
    }

    return 0;
}
