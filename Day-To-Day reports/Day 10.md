# **Day 10:**

### **Break statement:**

When the iterator see's break statement it jumps out of the loop.

Ex:

```python
for i in range(10):
    if i % 2:
        break
    print(i)
```

Output will be:

0

* Break statement in python only jumps out of the immediate loop.

### Continue statement:



```python
#Program example for continue statement
for i in range(10):
    if i % 2:
        continue
    print(i)
```

Output will be:

0

2

4

6

8

### **Else statement:**

Pass statement:

```python
n = int(input())
if n % 2 == 0:
    pass
else:
    print("Example for pass")
```

### **Ternary operator:**

The ternary operator is an operator that takes three arguments. The first argument is a comparison argument, the second is the result upon a true comparison, and the third is the result upon a false comparison. Ternary operator is shortened way of writing an if-else statement.

+ There is no ternary operator in python, but can be obtained indirectly.

```python
print("Odd" if int(input()) % 2 else "Even")
```

### **String Functions & Methods:**

+ Function is not associated with an object.
+ Method is a function that belongs to an object. It is used to manipulate that object.

