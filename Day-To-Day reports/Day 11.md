# **Day 11:**

### Methods:

A method is a function that “belongs to” an object.

Ex:

```python
string = "that's life"
string = string.capitalize() #.capitalize() is a method, string is the object.
print(string)
```

Output will be:

That's life

### **Other methods:**

To be used along with a string name. Such as string.title()

* .title() - Will change first letter of all words into uppercase.

* .swapcase() - Will change uppercase to lowercase and lower case to uppercase in a string.

* .upper() - will change all letters into uppercase.

* .lower() - will change all letters into lowercase.

* .isupper() - Returns True if all letters are un uppercase else False

* .islower()

* .isalpha() - Returns true if

* .isalnum()

* .isspace()

* .isdigit()

* .center(num) - string.center(20)- Center justification in taking total 20 spaces.

* .ljust(num) - Left justification

* .rjust(num)

* .zfill(num) - string.zfill(20)

* .count() - Ex: string.count('o') - Will count number of 'o' present in string. Also a word can be counted.

  string.count("is",10) - Will count number of times "is" appears before index 10.

  string.count("is",10,20) - Counts between index 10 to 20

+ .startswith("Python") - Checks if the string starts with "Python".

+ .endswith("ing") - Checks if the string ends with "ing".

+ .find("is") - Checks if "is" is present in the string. Returns the index value after which "is" is present in the string. Returns -1 if not present.

  Returns value if "is" is present even in between words like in "This"

+ .index("is") - Returns the index of "is" in the string. If not gives an error.

+ list(<string name>) - Will convert string into list.

+ " ".join(<string or list name>) - Will join a iterable without any spaces. Cannot join numbers.

+ .strip() - Will remove the spaces on left and right side of the string.

+ .lstrip() & .rstrip()

+ .split("string") - Will convert a sentence in to a list with each word as elements.

+ .split("string",number) - Will split upto

+ .rsplit("string",number) - Reverse split. Will split from last

+ <stringname>.translate("aei ou","123456")  -  Will replace "a" in string with "1", "e" with "2", " " with "4", respectively.

