http://localhost:8889/lab/tree/bank_account_code.ipynb
class Bank:
    def __init__(self):
        self.balance=0
        print("BOB")

    def account_number(self):
        while True:
            account_number=int(input("enter account_number"))
            if account_number==123: 
                print("welocome to bank")
                break
        
            else:
                print("account_number not exist")
                break
            
    def deposite(self):
        amount=int(input("enter the amount to deposite"))
        self.balance=amount + self.balance
        print(self.balance)
    print("1.deposite")

    def withdrawl(self):
        amount=int(input("enter the amount to withdrawl"))
        if self.balance-amount<0:
            print("inalid amount")
        else:
            self.balance=self.balance - amount
            print(self.balance)
    print("2.withdrawl")
    

    def getbalance(self):
        print(self.balance)
    print("3.balance")
    
bank=Bank()
while True:
    bank.account_number()
    what=int(input("enter the option"))
    if what==1:
        bank.deposite()
    elif what==2:
        bank.withdrawl()
    elif what==3:
        bank.getbalance()
    else:
        print("invalid input")
