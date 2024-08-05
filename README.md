import time
print('insert your card')
time.sleep(5)
password = 1234
balance = 5000
pin = int(input('enter your atm pin'))
if password == pin:
    while True:
        print('''
            1 == check balance
            2 == withdraw money
            3 == deposit money
            4 == exit
            ''')
        print('-------------------------------------------------------')
        try:
            option = int(input('please enter your choice'))
        except:
            print('please enter valid option')
        if option == 1:
            print(f'your current balance is {balance}')
            print('-------------------------------------------------------')
        if option == 2:
            withdraw_amount = int(input('please enter withdraw amount'))
            print('-------------------------------------------------------')
            balance -= withdraw_amount
            print(f'{withdraw_amount} is debited from your account')
            print('-------------------------------------------------------')
            print(f'your updated balance is {balance}')
            print('-------------------------------------------------------')
        if option == 3:
            deposit_amount = int(input('please enter deposit amount'))
            print('-------------------------------------------------------')
            balance += deposit_amount
            print(f'{deposit_amount} is credited into your account')
            print('-------------------------------------------------------')
            print(f'your updated balance is {balance}')
            print('-------------------------------------------------------')
        if option == 4:
            break
else:
    print('wrong pin please try again')
