# **Day 12:**

### String methods continued:

* format()  - The format() method formats the specified value(s) and insert them inside the string's placeholder.

  The placeholder is defined using curly brackets: {}. Read more about the placeholders in the Placeholder section below.

  The format() method returns the formatted string.

* max(<list>) - Returns the maximum number from the list

* any(<list>) - Returns false if all the numbers in the list are zero. Returns true if any one or all number in the list are non zero.

* <list>.pop(<index>) - Will remove the element from the list and returns the element.

* <list>.remove(<index>) - Will delete the element from the list. Doesn't return the value.

* <list>.reverse() - Will reverse the entire list.

* <list>.sort(reverse=True) - Will sort the list descending order.

* <list2> = <list1>.copy() -Will create a new list "list2" with contents of "list1"

  But, list2 = list1 will not create a new list but will just assign the name list 2 with memory location of list1.

### **List comprehension:**

Syntax:

<list_obj> = [<expr> for <iter_variable> in <iterator> ]

* List comprehension with if statement:

<list_obj> = [<expr> for <iter_variable> in <iterator> if <condition>]

```python
# program to find a square of list of elements
print(*[int(i)**2 for i in input().split(" ") if i != "" and int(i)%2 == 0])
# some random if statements in one line
print(*[int(i)**2 if int(i)%2 == 0 else int(i) for i in input().split(" ") if i != "" and int(i) >= 1 and int(i) <= 100])
```

