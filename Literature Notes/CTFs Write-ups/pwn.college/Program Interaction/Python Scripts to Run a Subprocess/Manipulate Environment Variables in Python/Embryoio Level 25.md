This program requires to be run in a python script with the environment variable **kexugp** with value *dyllawfhll*.

Steps to solution:
	1) Create a Python script 
	2) Run a subprocess as shown in
	3) Create an environment variable similar to , but with a variable set rather than just an empty dictionary

Solution:
```python
	# Importing subprocess to run external executables
	import subprocess
	
	# Run the program
	# Set the environment variable kexugp equal to dyllawfhll
	subprocess.run("./embryoio_level25", env = {"kexugp" : "dyllawfhll"})```

The flag is:
	pwn.college{4MEf9dlao4jQqNYoKAig_eq6L-w.dVjMsQDMwUzW}