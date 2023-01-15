This program requires a Python subprocess that redirects stdin from **/tmp/icuett** with input **.

Steps to solution:
	1) Create a Python script
	2) Run a subprocess as in 
	3) Redirect stdin as shown in [[Embryoio Level 5]] and 

Solution:
```python
	import subprocess

	with open("/tmp/icuett", "r+") as tt:
		subprocess.run("./embryoio_level26", stdin=tt)
```
```bash
	touch /tmp/icuett ; echo -ne "mshdrnzt" > /tmp/icuett ; python /tmp/my_script.py
```

The flag is:
	*pwn.college{0CFe_bQwnLsSibome2ge1e1caW7.dZjMsQDMwUzW}*