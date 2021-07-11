Some prime numbers can be expressed as a sum of other consecutive prime numbers.
For example

5 = 2 + 3,

17 = 2 + 3 + 5 + 7,

41 = 2 + 3 + 5 + 7 + 11 + 13.

Your task is to find out how many prime numbers which satisfy this property are present in the range 3 to N subject to a constraint that summation should always start with number 2.

Write code to find out the number of prime numbers that satisfy the above-mentioned property in a given range.



```python
def isprime(num):
    val = True
    if num > 1:
        for i in range(2, num):
            if (num%i) == 0:
                val = False
                break
        else:
            val = True
    return val

num = int(input())
sum = 0
primelist = []
if 2<num<12000000000 and isprime(num) == True:
    foo = [int(i) for i in range(2, num) if isprime(i)]
    for i in foo:
        if sum < num:
            sum += i
            if sum <= num: primelist.append(i)

if sum == num:
    print(num,"= ",end="")
    print(*primelist,sep=" + ")
```