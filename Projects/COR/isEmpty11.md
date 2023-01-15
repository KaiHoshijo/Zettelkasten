202212151745
Status: #project
Tags: #CTF #COR #Ghidra #Function 

# isEmpty11

It iterates from 0 to 0xb and checks if the offset at [[0x14000d008]] is equal to zero.

This function will be checking the processes set from [[tls_callback_0]] and will cause the program to exit if any of them are found.



---
# References