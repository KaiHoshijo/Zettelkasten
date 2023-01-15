202212151734
Status: #project 
Tags: #CTF #COR #AntiDebuggingEmporium #Ghidra #Function

# checkFlag

First off, it has a for statement that iterates 0x44 times, which adds the values at [[0x14000dbe0]] and [[0x14000db90]] and stores the result into [[0x14000db90]].

Next, it prints a new line to the user.

For the center part of the loop, it iterates j starting at 0 until it reaches 0x3f. However, it increments j by 4, so it be the following values:
    0, 4, 8, 12, 16, 20, 24, 28, 32, 36, 40, 44, 48, 52, 56, 60

This will check the input from the user (xor'ed with [[0x14000db88]]) to [[0x14000db90]] and will exit the loop if the user is wrong.

In the case that the user is wrong, [[printRandom]] is called.

---
# References