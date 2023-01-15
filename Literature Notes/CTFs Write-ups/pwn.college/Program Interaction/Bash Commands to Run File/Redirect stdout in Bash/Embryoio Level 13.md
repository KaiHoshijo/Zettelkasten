This program, ran in Bash, requires the stdout to be redirected to */tmp/xhzsit*.

Steps to solution:
	1) Run program like in [[Embryoio Level 8]]
	2) Redirect output like in [[Embryoio Level 6]]

Solution:
```bash
#!/bin/bash

./embryoio_level13 > /tmp/xhzsit ; cat /tmp/xhzsit
```

Flag:
	*pwn.college{k78aE8OXK53eGvIw-SGjidjTXch.dNTMsQDMwUzW}*