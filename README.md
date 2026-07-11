# python-conditional-statements
#if
# Bank Balance Penalty System

balance = float(input("Enter Account Balance: "))

minimum_balance = 5000

if balance < minimum_balance:
    balance = balance - 250

print("Updated Balance:", balance)al_bill)


#if-else
# Loan Approval Based on Credit Score

credit_score = int(input("Enter Credit Score: "))

if credit_score >= 700:
    print("Loan Approved")
else:
    print("Loan Rejected")
    print("Reason: Credit Score is below 700")


#if-elif-else
# Income Tax Calculator

income = float(input("Enter Annual Income: "))

if income <= 250000:
    tax = 0
elif income <= 500000:
    tax = income * 0.05
elif income <= 1000000:
    tax = income * 0.20
else:
    tax = income * 0.30

net_income = income - tax

print("Tax Amount:", tax)
print("Net Income:", net_income)


# Electricity Bill Generator

units = int(input("Enter Units Consumed: "))

if units <= 100:
    bill = units * 1.5
elif units <= 300:
    bill = units * 3
elif units <= 500:
    bill = units * 5
else:
    bill = units * 8

gst = bill * 0.18
total_bill = bill + gst

print("Bill Amount:", bill)
print("GST:", gst)
print("Total Bill:", total_bill)


#nested-if
# Loan Approval System

age = int(input("Enter Age: "))
salary = float(input("Enter Monthly Salary: "))
credit_score = int(input("Enter Credit Score: "))

if age >= 21:
    if salary >= 30000:
        if credit_score >= 750:
            print("Loan Approved")
        else:
            print("Loan Rejected")
            print("Reason: Credit Score below 750")
    else:
        print("Loan Rejected")
        print("Reason: Salary below 30000")
else:
    print("Loan Rejected")
    print("Reason: Age below 21")


# University Placement Eligibility

cgpa = float(input("Enter CGPA: "))
backlogs = int(input("Enter Number of Backlogs: "))
communication_score = int(input("Enter Communication Score: "))

if cgpa >= 7.0:
    if backlogs == 0:
        if communication_score >= 7:
            print("Eligible for Placement Drive")
        else:
            print("Not Eligible")
            print("Reason: Communication Score below 7")
    else:
        print("Not Eligible")
        print("Reason: Backlogs must be 0")
else:
    print("Not Eligible")
    print("Reason: CGPA below 7.0")



# Check Triangle Validity and Type

side1 = float(input("Enter first side: "))
side2 = float(input("Enter second side: "))
side3 = float(input("Enter third side: "))

if (side1 + side2 > side3) and (side1 + side3 > side2) and (side2 + side3 > side1):

    print("Valid Triangle")

    if side1 == side2 == side3:
        print("Type: Equilateral Triangle")
    elif side1 == side2 or side1 == side3 or side2 == side3:
        print("Type: Isosceles Triangle")
    else:
        print("Type: Scalene Triangle")

else:
    print("Invalid Triangle")


# ATM Withdrawal System

correct_pin = 1234
balance = 50000
daily_limit = 10000

pin = int(input("Enter PIN: "))
amount = float(input("Enter Withdrawal Amount: "))

if pin == correct_pin:
    if amount <= daily_limit:
        if amount <= balance:
            balance = balance - amount
            print("Transaction Successful")
            print("Amount Withdrawn:", amount)
            print("Remaining Balance:", balance)
        else:
            print("Transaction Failed")
            print("Reason: Insufficient Balance")
    else:
        print("Transaction Failed")
        print("Reason: Daily Limit Exceeded")
else:
    print("Transaction Failed")
    print("Reason: Incorrect PIN")

