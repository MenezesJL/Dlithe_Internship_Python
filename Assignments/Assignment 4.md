# Assignment 4

**Problem 1:** Given the participants' score sheet for your University Sports Day, you are required to find the runner-up score. You are given N scores. Store them in a list and find the score of the runner-up.

```python
n = int(input())
score = map(int,input().split())
sort = list(set(list(sorted(score))))
print(sort[-2])
```

**Problem 2:** Rotate a given String in the specified direction by specified magnitude.
After each rotation make a note of the first character of the rotated String, After all rotation are performed the accumulated first character as noted previously will form another string, say FIRSTCHARSTRING.
Check If FIRSTCHARSTRING is an Anagram of any substring of the Original string.
If yes print "YES" otherwise "NO". Input
The first line contains the original string s. The second line contains a single integer q. The i'th of the next q lines contains character d[i] denoting direction and integer r[i] denoting the magnitude.

```python
# Functions to check for counts:
def areCountEqual(c1, c2):
    for k in c1:
        if k not in c2 or c1[k] != c2[k]:
            return False
    return True
#Fnction to get character count:
def getCharCounts(s):
    counts = dict()
    for char in s:
        if char not in counts:
            counts[char] = 1
        else:
            counts[char] +=1
    return counts
#Function to check if string "A" is anagram of string "B":
def isAnagram(A,B):
    if len(A) < len(B):
        return False
    countB = getCharCounts(B)
    for i in range(0, len(A) - len(B) + 1):
        window = A[i : i +len(B)]
        countwindow = getCharCounts(window)
        if areCountEqual(countB, countwindow):
            return True
    return False

# Main program:
word = input().strip()
firstChar = []
index = 0
foo = int(input())
for _ in range(foo):
    direc, s= input().strip().split()
    s = int(s)
    if direc == "L":
        index = (index+s) % len(word)
    else:
        index = (index-s) % len(word)
    firstChar.append(word[index])
if isAnagram(word, firstChar):
    print("Yes")
else:
    print("No")
```

**Problem 3:**  In English alphabets there are two types of words, vowels and consonants. You are writing a program to reverse a given string, but the vowels are stubborn to move away from their position. So given a string where the vowels are stubborn,
print what will be word if the entire word is reversed except for the vowels.

```python
while True:
    bar = input()
    if len(bar) >= 3 and len(bar) <= 10**5:
        break
    else:
        print("Enter a word which contains at least 3 letters")
ree = []
j = ""
for i in bar:
    if i in "aeiou":
        ree.append(j)
        j = ""
        ree.append(i)
    else:
        j += i
if j != "": ree.append(j)
print(*ree[::-1],sep="")
```

**Problem 4:**  Array of integers is a hill, if:

it is strictly increasing in the beginning; after that it is constant; after that it is strictly decreasing.
The first block (increasing) and the last block (decreasing) may be absent. It is allowed that both of this blocks are absent.

```python
n = int(input())
bar = list(map(int,input().split()))
if len(bar) == 1:
    print("Yes")
else:
    prev_val = bar[0]
    surface = False
    for i in range(1, len(bar)):
        if prev_val == bar[i]:
            surface = True
        elif prev_val > bar[i] and not surface:
            print("No")
            break
        elif prev_val < bar[i] and surface:
            print("No")
            break
        prev_val = bar[i]
    else: print("Yes")
```

**Problem 5:** A little girl living in a village craves some rava idli even though she has had rava idli for the last 346514534 days in a row !! At the idli shop there are two types of Rava Idli's available. One goes for Rs.A per piece and the other goes for Rs.B per piece. The girl has a total of K rupees. What is the maximum number of rava idlis that she can have?

```python
test_case = int(input("Enter number of test cases between 1 & 1000:\n"))
if test_case >= 1 and test_case <= 1000:
    list1 = []
    print("Input :\nEnter A, B and K values:")
    for i in range(test_case):
        a, b, k = map(int, input().split())
        if a >= b:
            list1.append(int(k / b))
        else:
            list1.append(int(k / a))
    print("Output :")
    for n in range(test_case):
        print(list1[n])
else:
    print("Invalid input!!")
```

**Problem 6:** Python program to remove Nth occurrence of the given word. Given a list of words in Python, the task is to remove the Nth occurrence of the given word in that list.

```python
bar = input("list = ").split(" ")
word = input("word = ")
n = int(input("N = "))
count = 1
print(len(bar))
for i in range(len(bar)):
    if bar[i] == word:
        if n == count:
            bar.pop(i)
            break
        count += 1
print(bar)
```

**Problem 7:** Reverse words in a given String in Python

```python
foo = input().split(" ")
foo.reverse()
print(*foo,sep = " ")
```

**Problem 8:** Check if a Substring is Present in a Given String

```python
print("yes" if input("s1 = ").lower() in input("s2 = ").lower() else "no")
```

**Problem 9:** Python program to print even length words in a string

```python
print(*[i for i in input().split(' ') if len(i) % 2 == 0],sep = "\n")
```

**Problem 10:** Program to check if a string contains any special character(defined special character set)

```python
bar = input()
special = "!@#$%^&*()_+-~"
for i in bar:
    if i in special:
        print("String is not accepted")
        break
else:
    print("String is accepted")
```

