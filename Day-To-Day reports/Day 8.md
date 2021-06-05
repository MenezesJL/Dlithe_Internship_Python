# **Day 8**

## Nested loops:

syntax:

```python
for <iter_var> in <iteration>:
    for <iter_var> in <iteration>:
        <statements>
```

* 1st loop is called outer loop

* 2nd and other loops inside 1st loop are inner loop

#### Example program:

```python
# Pattern 1+3:
# Program to print the following pattern
# Input : Sam
# Output :
# S    S
# Sa  Sa
# SamSam

string = input()
size = len(string)
for index in range(1,size+1):
    # print(string[:index], end="")
    # print(" " * ((size-index)*2), end="")
    # print(string[:index])
    # print(string[:index] + " " * ((size-index)*2) + string[:index])
    print(string[:index] + " " * ((size-index)*2) + string[:index][::-1])
```

