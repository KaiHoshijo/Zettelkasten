This program requires the stdin to be redirected from file *wsleqh* with input **hfdsnuwk**

This utilizes the Linux command **<** to take input from a file and pass it into another's request for input.

Steps to get flag:
	1) Run file like [[Embryoio level 1]]
	2) Redirect input from file *wsleqh*
	3)  Pass **hfdsnuwk** to stdin like [[Embryoio Level 2]]

The solution is as follows:
```bash
	touch /tmp/wsleqh ; echo -ne "hfdsnuwk" > /tmp/wsleqh ; ./embryoio_level5 < /tmp/wsleqh
```

The flag is:
	*pwn.college{MMQvjNl967gtG2hnyOhWqtxma35.0VNsQDMwUzW}*