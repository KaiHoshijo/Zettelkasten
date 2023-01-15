202212141103
Status: #literature 
Tags: #linux #pwncollege #privilegeescalation 

# How Different UIDs have Different Privileges
Each user id (UIDs) have different privileges. A normal user will have a UID of 1000 or something similar, which prevents them from running certain processes (like apt) or remove certain files.

The UID 0 is root, which gives all control of the file system.





---
# References
1. Program Misuse - Privilege Escalation on pwn.college at "4:39"