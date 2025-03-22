# Bank_application

import time
def show_balance():
    print("=====================BALANCE=============================")
    print(f"Your balance is ${balance:.2f}")
    print("=====================BALANCE=============================")



def deposit():
    print("********************DEPOSIT*****************************")
    amount=float(input("Enter an amount to be Deposited: "))
    print("********************DEPOSIT*****************************")

    if amount < 1:
        print("That's not a valid amount")
        return 0
    else:
        return amount




def withdraw():
    print("!!!!!!!!!!!!!!!!!!WITHDRAWAL!!!!!!!!!!!!!!!!!!!!!!!")
    amount=float(input("enter amount to be withdrawn: "))
    print("!!!!!!!!!!!!!!!!!!WITHDRAWAL!!!!!!!!!!!!!!!!!!!!!!!")


    if amount>balance:
        print("Insufficient_funds")
        return 0
    elif amount<0:
        print("Amount must be greater than Zero")
        return 0
    else:
        return amount


balance=0
is_running=True


while is_running:
    print("*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*")
    print("=====WELCOME TO ICICI_ATM!!!=====")
    print("1.show_balance")
    print("2.deposit")
    print("3.Withdraw")
    print("4.Exit")
    print("*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*=*")


    print("==========================================")
    choice=input("enter your choice (1-4):")
    print("==========================================")



    if choice == '1':
        show_balance()
    elif choice == '2':
        balance += deposit()
    elif choice == '3':
        balance -= withdraw()
    elif choice == '4':
        is_running = False
    else:
        print("That is not a valid")

print("!!!!!!!!!!!!!!!!!!!!!!!!!!!!Greeting from ICICI ATM!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!")
print("***************!!!Thankyou have a nice day!!!*****************")        
print("!!!!!!!!!!!!!!!!!!!!!!!!!!!!Greeting from ICICI ATM!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!")
