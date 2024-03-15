# ATM Simulator

## Problem Description
You are tasked with simulating an ATM (Automated Teller Machine) system. The ATM should allow users to perform basic banking transactions such as checking balance, depositing funds, and withdrawing funds.

## Input
The input will consist of a sequence of commands, each specifying a transaction to be performed by the user. The commands may include:
- "check_balance": Check the current balance in the user's account.
- "deposit <amount>": Deposit the specified amount into the user's account.
- "withdraw <amount>": Withdraw the specified amount from the user's account.

## Output
The output will contain the result of each transaction, including the updated balance after each deposit or withdrawal.

## Constraints
- The initial balance in the user's account is non-negative.
- The amount specified in the "deposit" and "withdraw" commands will be positive integers.
- The ATM should prevent overdrafts (i.e., withdrawing more funds than the current balance).

## Examples
|Input|Output|
|-|-|
|check_balance|Balance: $100|
|deposit 50|Deposit Successful. New Balance: $150|
|withdraw 30|Withdrawal Successful. New Balance: $120|