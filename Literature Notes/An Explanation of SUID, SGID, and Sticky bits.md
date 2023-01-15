202212141100
Status: #literature
Tags: #pwncollege #linux #privilegeescalation

# An Explanation of SUID, SGID, and Sticky bits

The effective (e) UID or GID is what lets a program run related to root, which is what is used to get Privilege Escalation through something like /usr/bin/cat or something else.

Fundamentally, these three have the same purpose in the Linux Permission model. They change the respective eUID, eGID, or limit file removal. This is set when a file is provided with levels related to the suid binary.



---
# References
1. Program Misuse - Privilege Escalation on pwn.college at "7:44"
