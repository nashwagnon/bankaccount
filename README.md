# bankaccount
# Bank Account in Python from Computer Science 235



class savings():
    def __init__(self,Deposit, Pin):
        self.balance = Deposit
        self.pin = Pin

    def getBalance(self, Pin):
        if Pin == self.pin:
            return self.balance
        else:
            return False
            print("0")

    def displayBalance(self, Pin):
        if self.pin == Pin:
            print ("Balance is $.2f." % self.balance)
        else:
            print ("Transaction Failed")

    def deposit(self, Amount):
        # always accept money, no pin is needed
        self.balance = self.balance + Amount

    def withdraw(self, Amount, Pin):
        if self.pin == Pin:
            try:
                if self.balance - Amount >= 0:
                    self.balance -= Amount
                    return True
                else:
                    Return False

    def changePin(self, OldPin, NewPin):
        if OldPin == self.pin:
            return True
        else:
            return False
