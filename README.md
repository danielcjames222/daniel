# ALL 10 ASSIGNMENTS IN ONE FILE

# ────── Salary Calculator ──────
print("1. Salary Calculator")
salary = float(input("Enter basic salary: "))
bonus = float(input("Enter bonus: "))
tax_rate = float(input("Enter tax rate (e.g. 0.1 for 10%): "))

gross = salary + bonus
tax = tax_rate * gross
net = gross - tax

print(f"Gross: ₦{gross:,.2f}")
print(f"Tax: ₦{tax:,.2f}")
print(f"Net Pay: ₦{net:,.2f}\n")

# ────── Login System (3 Attempts) ──────
print("2. Login System")
username = "Promise"
password = "12345"
attempts = 3

while attempts > 0:
    user = input(f"Enter username ({attempts} attempts left): ")
    pwd = input("Enter password: ")
    if user == username and pwd == password:
        print("Welcome back!\n")
        break
    else:
        attempts -= 1
        if attempts > 0:
            print("Wrong credentials. Try again.\n")
        else:
            print("Account locked\n")

# ────── Student Grade Analyzer ──────
print("3. Student Grade Analyzer")
scores = []
for i in range(4):
    score = int(input(f"Enter score {i+1}: "))
    scores.append(score)

average = sum(scores) / 4
highest = max(scores)
lowest = min(scores)

if average >= 70:
    grade = "A"
elif average >= 60:
    grade = "B"
elif average >= 50:
    grade = "C"
else:
    grade = "F"

print(f"Average: {average}")
print(f"Highest: {highest}")
print(f"Lowest: {lowest}")
print(f"Grade: {grade}\n")

# ────── ATM Withdrawal Simulation ──────
print("4. ATM Withdrawal")
balance = 5000
amount = float(input("How much do you want to withdraw? ₦"))

if amount <= 0:
    print("Invalid amount")
elif amount > balance:
    print("Insufficient funds")
else:
    balance -= amount
    print(f"Withdrawal successful! New balance: ₦{balance:,.2f}\n")

# ────── Membership Login ──────
print("5. Membership Login")
members = ("Favor", "Blessing", "Joy")
pwd = "abc123"

name = input("Enter your name: ").strip()
entered_pwd = input("Enter password: ")

if name in members:
    if entered_pwd == pwd:
        print("Access granted")
    else:
        print("Password incorrect")
else:
    print("Not registered\n")

# ────── Phone Network Checker ──────
print("6. Phone Network Checker")
number = input("Enter phone number (11 digits): ").strip()

if number.startswith(("070", "080", "081", "090", "091")):
    if number.startswith(("070", "080")):
        network = "MTN"
    elif number.startswith("081"):
        network = "Airtel"
    elif number.startswith(("090", "091")):
        network = "Glo"
    else:
        network = "Unknown"
else:
    network = "Unknown network"

print(f"Network: {network}\n")

# ────── Two-Number Comparison ──────
print("7. Two-Number Comparison")
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

if a > b:
    print(f"{a} is larger")
elif b > a:
    print(f"{b} is larger")
else:
    print("They are equal")

total = a + b
print(f"Sum is {'even' if total % 2 == 0 else 'odd'}\n")

# ────── Shopping Discount Program ──────
print("8. Shopping Discount")
price = float(input("Enter unit price: ₦"))
quantity = int(input("Enter quantity: "))

total = price * quantity
discount = 0

if total >= 20000:
    discount = total * 0.10
    final = total - discount
    print(f"Congratulations! You get 10% discount")
else:
    final = total
    print("No discount applied")

print(f"Subtotal: ₦{total:,.2f}")
print(f"Discount: ₦{discount:,.2f}")
print(f"Final Amount: ₦{final:,.2f}\n")

# ────── Bus Fare System ──────
print("9. Bus Fare System")
full_price = 500  # assuming base fare

age = int(input("Enter passenger age: "))
is_student = input("Are you a student? (yes/no): ").lower()

if age < 10:
    fare = 0
    print("Free ride!")
elif is_student == "yes":
    fare = full_price / 2
    print("Student discount applied")
elif age <= 17:
    fare = full_price / 2
    print("Youth fare")
else:
    fare = full_price

print(f"Fare: ₦{fare}\n")

# # ────── Electricity Bill Calculator ──────
print("10. Electricity Bill Calculator")
units = int(input("Enter units consumed: "))
bill = 0

if units <= 100:
    bill = units * 25
elif units <= 200:
    bill = 100 * 25 + (units - 100) * 35
else:
    bill = 100 * 25 + 100 * 35 + (units - 200) * 45

print(f"Total Bill: ₦{bill:,}\n")

print("All 10 questions completed successfully! You're a legend!")
