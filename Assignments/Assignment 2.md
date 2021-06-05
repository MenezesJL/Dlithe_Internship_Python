# Assignment 2

```python
#Problem 1: Given an integer,n, perform the following conditional actions:
#If n is odd, print Weird, 
#If n is even and 
#    in the inclusive range of 2 to 5, print Not Weird 
#    If n is even and in the inclusive range of 6 to 20, print Weird 
#    If n is even and greater than 20, print Not Weird

n = int(input("Enter an integer:"))
if n % 2 == 0 and n >= 1 and n <= 100:
    if n >= 2 and n <= 5 or n > 20:
        print("Not Weird")
    elif n >= 6 and n<= 20:
        print("Weird")
else:
    print("Weird")
```

```python
#problem 2:Read three integers from the keyboard a,b,c, d and those values in the following order: max > mid1 > mid2 > min

list1 = list(map(int, input("Enter 4 integers :").split()))
print(list1)
a, d = min(list1), max(list1)
list1.remove(a)
list1.remove(d)
b, c = min(list1), max(list1)
print(d, c, b, a,sep=" > ")
```

```python
#problem 3: Write a program to calculate the EB Bill.
#The tariff rate for all division is the same. Karnataka electricity board single slaps for the domestic LT supply such as for 0 to 30 units the per-unit cost will be 3.75/-, from 31 to 100 the per-unit cost will be 5.20, from 101 to 200, the per-unit cost will be 6.75 and above 201 units you have to pay 7.8 per unit.
#Additionally, the consumer will pay fixed charges as 60/- and electricity tax of 5% extra.

unit = int(input("Enter number of units:"))
bill = 0
if unit in range(0, 31):
    bill = 3.75 * unit
if unit in range(31, 101):
    bill = 5.20 * unit
if unit in range(101, 201):
    bill = 6.75 * unit
if unit >= 201:
    bill = 7.8 * unit
tax = bill * 5 / 100
total_amount = bill + tax + 60
print("No. of Units  :%10.2f"%float(unit))
print("Bill amount   :%10.2f"%float(bill))
print("Tax           :%10.2f"%float(tax))
print("Fixed charge  :%10.2f"%float(60))
print("Total payable :%10.2f"%float(total_amount))
```

```python
#Problem 4: Write a program to calculate the grade.
#Constraints: Score should be in between 1 to 100

score = int(input("Enter the score :"))
if score in range(1, 101):
    if score < 50:
        print("No Grade")
    if score in range(50, 60):
        print("Grade B")
    if score in range(60, 70):
        print("Grade B+")
    if score in range(70, 80):
        print("Grade A")
    if score in range(80, 90):
        print("Grade A+")
    if score >= 90:
        print("Grade O")
else:
    print("Enter a valid grade")
```

```python
#Problem 5: Program to find whether the entered year is leap year in Georgian calendar.
#The year can be evenly divided by 4, is a leap year, unless:
#The year can be evenly divided by 100, it is NOT a leap year, unless:
#The year is also evenly divisible by 400. Then it is a leap year.
#This means that in the Gregorian calendar, the years 2000 and 2400 are leap years, while 1800, 1900, 2100, 2200, 2300 and 2500 are NOT leap years.

year = int(input("Enter the year to check if its leap year:"))
if year % 4 == 0:
    if year % 100 == 0:
        if year % 400 == 0:
            print("Yes")
        else:
            print("No")
    else:
        print("Yes")
else:
    print("No")
```

