# Assignment 1

**Problem 1:** Write a program to calculate simple interest.

```python
P = int(input("Enter the principal amountS :"))
R = float(input("Enter interest rate        :"))
N = float(input("Enter number of years      :"))
interest = (P*N*R)/100
print("Simple interest is         :", round(interest, 2))
```



**Problem 2:** Program to find sum and average of 3 numbers.

```python
a, b, c = map(int, input("Enter 3 numbers:").split())
Sum = a + b + c
Avg = Sum/3
print()
print("Sum of the numbers :", Sum)
print("Average :", round(Avg, 3))
```



**Problem 3:** Write a program to perform the following task:
The provided code stub reads two integers from STDIN, and . Add code to print three lines where:
The first line contains the sum of the two numbers.
The second line contains the difference of the two numbers (first - second).
The third line contains the product of the two numbers.

```python
a,b = map(int,input("Enter 2 numbers:").split())
print(a+b)
print(a-b)
print(a*b)
```



**Problem 4:** Read 3 integers a, b, c from the keyboard and arrange them in the order: max > mid > min.

```python
a, b, c = map(int, input("Enter 3 numbers:").split())
x = min(a, b, c)
z = max(a, b, c)
y = (a+b+c-x-z)
print(z, y, x, sep=">")
```



**Problem 5:** Read four values a,b,c,d from the keyboard and print the result of a^b + c^d in single line.

```python
a, b, c, d = map(int, input("Enter 4 integers:").split())
print(pow(a, b) + pow(c, d))
```

