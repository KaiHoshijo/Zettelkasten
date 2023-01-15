202212141112
Status: #project
Tags: #CTF #COR #Ghidra #Windows

# AntiDebuggingEmporium

There are two entry points for this program.

The first is entry, which is the standard entry point. 
* It sets the seed of rand to be random.
* Prints the "Please enter the flag: " string
* Reads a string in from the user
* Checks if the 11 settings from the other entry point is set to false in the [[isEmpty11]] function.
    * Calls the [[checkFlag]] function, which will check if the flag is valid or not.
* If the one of the 11 settings isn't false then [[printRandom]] is called

Additionally, the other entry point is [[tls_callback_0]], which will create a thread that will check for debugging programs.

---
# References