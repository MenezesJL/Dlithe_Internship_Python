# Day 6

## Iterative control structure:

syntax:

while <statement>:

Ex:

```python
#Program to print a message 100 times
cnt = 0
while cnt < 100:
    print("Test message")
    cnt += 1	
```

Example: Program to reverse a number

```python
while num:
    remainder = num %10
    print(remainder, end="")  # end="" prints next time in same line
    num //= 10
```

But the above code prints single integers without a space but its not a single number.

```python
num = int(input("Enter a number:"))
reverse = 0
while num:
    remainder = num % 10
    reverse = reverse * 10 + remainder
    num //= 10
print(reverse)
```

Reversing using string datatype

```python
#Program to reverse a number using string
num = input("Enter a number:")[::-1]
print(num)
```

## Range function:

ex: 	n = range(100)

```python
n1 = range(1,10)
print(*n1)
#1 2 3 4 5 6 7 8 9		will be the answer
```

if range should be from larger num to smaller num, then:

```python
n1 = range(10,1,-1)
print(*n1)
```

## **For loop:**

syntax:

for <iter_variable> in <iterator/sequence>:

​	<statement>

+ If the number of iterations is known for statement is better.

+ If number of iterations is nit known, then while statement is better.

Example:

```python
#program to print even numbers fron a list
#Getting the list of values from user
list1 = list(map(int, input("Enter list of numbers:").split()))

for element in list1:
    if not element % 2 :
        print(element)
```

Instructor told about string library.

+ character datatype isn't available in python.

```python
#program to print consonents
import string   #Importing string module
sentence = input("Enter a string:")
for char in sentence:
    if char in string.ascii_letters and char not in "aeiouAEIOU":
        print(char)
```

Another method to write above program:

```python
#program to print consonents
import string   #Importing string module
sentence = input("Enter a string:")
for char in sentence:
    if char.isalpha() and char not in "aeiouAEIOU":
        print(char, end="")
```

