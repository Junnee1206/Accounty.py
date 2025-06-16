# Accounty.py
class Account:
    def __init__(self):
        self_balance = 10000
        print("Account balance is: ",self_balance)
    def deposit(self, amount):
        self_balance = amount + self_balance
        print("Account balance is: ",self_balance)
    def withdraw(self, amount):
        self_balance = self_balance - amount
        print("Account balance is: ",self_balance)

class SavingsAccount(Account):
    def __init__(self):
        Account.__init__(self)
    def savingsWithdraw(self, amount):
        if(amount < 1000):
            super().withdraw(amount)
        else:
            print("Amount exceeds withdrawal limit")
savings = SavingsAccount()
savings.savingsWithdraw(2000)

class Current_Account(Account):
    def __init__(self):
        Account.__init__(self)
current = Current_Account()
current.withdraw(2000)
