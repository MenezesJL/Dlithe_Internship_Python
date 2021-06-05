# Assignment 3

**Program 1:** A little girl living in a village craves some rava idli even though she has had rava idli for the last 346514534 days in a row !! (Strange, you might think. But its normal down here)At the idli shop there are two types of Rava Idli's available.One goes for Rs.A per piece and the other goes for Rs.B per piece.The girl has a total of K rupees.What is the maximum number of rava idlis that she can have?Note that she does not care about the type of idli she gets, she just wants to have as many rava idlis of any type as possible.

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

**Problem 2:** You are given a positive integer . Print a numerical triangle of height like the one below:
1

22

333

4444

55555

......

Can you do it using only arithmetic operations, a single for loop and print statement?Use no more than two lines. The first line (the for statement) is already written for you. You have to complete the print statement.

```python
for i in range(1, int(input())):
    print(int(i * 10 ** i / 9))
```

**Problem 3:** You are given a rectangular board of M×N squares. Also you are given an unlimited number of standard domino pieces of 2×1 squares. You are allowed to rotate the pieces. You are asked to place as many dominoes as possible on the board so as to meet the following conditions:
1.Each domino completely covers two squares.
2.No two dominoes overlap.
3.Each domino lies entirely inside the board. It is allowed to touch the edges of the board.
Find the maximum number of dominoes, which can be placed under these restrictions.

```python
m, n = map(int, input("Enter values of m & n between 1 and 16:").split())
if 1 <= m <= n <= 16:
    dominoes = (m * n) /2
    print("The number of dominoes which can be placed in ",m,"x",n," size box are: ",int(dominoes))
else:
    print("Enter valid m & n values!")
```

**Problem 4:** Given an integer,n, perform the following conditional actions:
If n is odd, print Weird If n is even and in the inclusive range of 2 to 5, print Not Weird If n is even and in the inclusive range of 6 to 20, print Weird If n is even and greater than 20, print Not Weird

```python
n = int(input("Enter an integer between 1 & 100:\n"))
if n >= 1 and n <= 100:
    if n % 2 == 0:
        if n >= 2 and n <= 5 or n > 20:
            print("Weird")
        elif n >= 6 and n <= 20:
            print("Not Weird")
    else: print("Weird")
else: print("Invalid input!")
```

**Problem 5:** PRINT THE BELOW MENTIONED PATTERN FOR ANY "N" VALUE. WHERE "N" INDICATES NO.OF ROWS.

Sample Input:

5

Sample Output:

1   5

 2 4 

  3

```python
n  = int(input("Enter an odd number:\n"))
print("Output:")
if n % 2 != 0 and n >= 1 and n <= 100:
    bar = (n / 2) + 1
    space = [int(i) for i in range(n) if i % 2 != 0][::-1]
    num = n
    for i in range(n):
        print(" " * int(i), end='')
        print(i + 1, end="")
        if int(bar) == i + 1:
            print("")
            break
        else:
            print(" " * int(space[i]), end="")
            print(int(num))
        num -= 1
else:
    print("Invalid input!! Enter an odd number")
```

**Problem 6:** PRINT THE BELOW MENTIONED PATTERN FOR ANY "N" VALUE. WHERE "N" INDICATES NO.OF ROWS.

Sample Input:

5

Sample Output:
1

 2

  3

   4

​     5

```python
n = int(input())
if n >= 1 and n <= 100:
    for i in range(n):
        print(" "*int(i) + str(i+1))
```