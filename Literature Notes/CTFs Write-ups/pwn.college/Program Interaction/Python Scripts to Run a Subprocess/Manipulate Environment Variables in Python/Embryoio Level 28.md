This program, ran in Python, must ignore all environment variables.

Steps to solution:
	1) Run program like in [[]]
	2) Ignore environment variables like in [[]]

Solution:
```python
#!/bin/python

import subprocess

subprocess.run("./embryoio_level28", env = {})
```

Flag:
	*pwn.college{4iG4GohQ-BMCTF5teAPAM66YAti.dhjMsQDMwUzW}*