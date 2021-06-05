# Day 4

### Print function

```python
# for printing only two digits after decimal point
print("%.2f" % x)
```

### Dictionary datatype:

 It stores key, value pair data.

```python
# Create empty dictionary
dict1 = {} # also can be created using dict()
dict1['name'] = "Sample"
dict1['score'] = 9.9
print(dict1)

# Output would be
# {'name':'Sample','score':'9.9'}
```

* Dictionary keys are immutable, but their values are mutable

```python
tinydict = {'name':'Corvus','score':8.5}
# Displaying keys
print(tinydict.keys())
# Displaying values
print(tinydict.values())
# Command To delete key and value pair
del tinydict['score']
```

* Keys are case sensitive.
* del command is used to delete an element in dict. (There are other methods)

### List and Input functions:

```python
# List unpacking using split() function
a,b,c = input().split()
print(a,b,c)
```

### Higher Order Function:

* A function that can accept function as an argument
* map() is a higher order function.

```python
# Creating a list A with its elements as integers
A = list(map(int, input().split(" ")))
```

### Be a good programmer:

3 rules to follow to be a good programmer:

- Time efficiency
- Space efficiency
- Code optimization