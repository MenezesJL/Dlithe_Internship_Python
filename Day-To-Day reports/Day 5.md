# Day 5

## **Conditional control statements:**

No unconditional control statement in python as in C

Types of control statements:

 	1. Sequential
 	2. Selective
 	3. Iterative

Selective control statements example:	

A program contains calculation of both compound and simple interest, and the user can select any one type of interest to calculate.

### **If statement:**

syntax:

if<condition>:   #bracket for condition is not compulsory

​	<statements>

else:

​	<statements>

Example program:

```python
#%10.2f is the string modulus 
#program to calculate the bill
product_name = input("Product name:")
price = int(input("Price:"))
qty = int(input("Quantity:"))
amount = price * qty
discount = 0
if amount >= 5000:
    discount = amount * 15/100
net_amount = amount - discount
print("Bill amount : %10.2f"%float(amount))
print("Less (-)    : %10.2f"%float(discount))
print("------------")
print("Net amount  :%10.2f"%float(net_amount))
print("------------")
```

* In %10.2f , 10 means there will be 10 spaces before decimal point & 2 digits after 

```python
#program to calculate the interest (Simple and compound)
principal = int(input("Principal :"))
rate = float(input("Rate of interest :"))
year = float(input("Number of years :"))

print("1. Simple interest")
print("2. Compound interest")
choice = int(input("Enter your choice :"))
if choice == 1:
    interest = principal * rate * years / 100
else:
    interest = principal * (1 + rate * years / 100) ** years - principal
print("Interest : %.2f"%interest)
```

#### Nested if:

if<condition1>:

​	<statements>

​	if<condition2>:

​		<statements>

elif<condition3>:

​		<statements>

else:

​	<statements>

Example program:

```python
#program to check given num is divisible by 3:
num = int(input("Enter the number :"))
if num % 2 == 0:
    if num % 3 == 0:
        print(num, "is divisible by 2 & 3")
    else:
        print(num, "is divisible by 2 and not by 3")
elif num %3 == 0:
    print(num, "is divisible by 3 and not by 2")
else:
    print(num, "is not divisible by 2 & 3")
```

* Instructor suggested pythontutor.com to understand step by step execution.



if<condition1>and<condition2>and<condition3>

​			<statements>

else:

​			<statements>

Example:

```python
a = 10  	    #value is non zero

b = not a

print(b)  		#output will be False
```

* Remember: Logical operators are called short circuit operators.

