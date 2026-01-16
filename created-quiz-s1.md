# Problem Statement
The two decided to create a program to implement "a function that warns them to make new candies when the number of candies that can be sold decreases below a certain number as candies are sold." Create the correct program.

# Answer
```
print("Enter inventory count")
n = int(input())
for i in range(n):
    n = n - 1
    if n == 0:
        print("Insufficient materials")
```
