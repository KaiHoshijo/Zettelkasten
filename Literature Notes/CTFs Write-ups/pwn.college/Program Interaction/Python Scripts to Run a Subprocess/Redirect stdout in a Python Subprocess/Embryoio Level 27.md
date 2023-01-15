This program, ran in Python, requires stdout to be redirected to */tmp/gshyjo*.

Steps to solution:
	1) Run program like in 
	2) Redirect stdout like in [[Embryoio Level 6]]

Solution:
```python
#!/bin/python

import subprocess

with open("/tmp/gshyjo", "w+") as gs:
	subprocess.run("./embryoio_level27", stdout=gs)

import os

os.system("cat /tmp/gshyjo")
```

Flag:
	*pwn.college{QgMHU1rpC1ouCQqb2g78EYKM4Oj.ddjMsQDMwUzW}*