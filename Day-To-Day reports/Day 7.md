# Day 7:

## Pattern printing programs:

* using len() function

```python
#Program to print the following pattern:
'''
Ramya
R
Ra
Ram
Ramy
Ramya
'''
string = input()
for index in range(len(string)):
    print(string[:index+1])
```

```python
#Program to print following pattern:
'''
input:text
Output:
text
tex
te
t
'''
string = input()
for i in range(len(string),0,-1):
    print(string[:i])
```

```python
#Program to print following pattern:
'''
input:text
Output:
   t
  te
 tex
text
'''
string = input()
for index in range(len(string)):
    print(" "*(len(string) - index - 1),end="")
    print(string[:index+1])
```

```python
#Program to print following pattern:
'''
input:text
Output:
texttext
tex  tex
te    te
t      t
'''
string = input()
size = len(string)
for index in range(size, 0, -1):
    print(string[:index],end="")
    print(" "*((size-index)*2),end="")
    print(string[:index])
```

```python
#Program to print following pattern:
'''
input:text
Output:
test
 tes
  te
   t
'''
string = input()
for index in range(len(string), 0, -1):
    print(" "*(len(string) - index),end="")
    print(string[:index])
```

```python
#Program to print following pattern:
'''
input:text
Output:
texttxet
tex  xet
te    et
t      t
'''
string = input()
size = len(string)
for index in range(size, 0, -1):
    print(string[:index],end="")
    print(" "*((size-index)*2),end="")
    print(string[:index][::-1])
```

