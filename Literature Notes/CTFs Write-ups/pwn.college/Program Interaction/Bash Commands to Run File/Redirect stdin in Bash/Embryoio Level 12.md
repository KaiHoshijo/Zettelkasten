This program, ran in Bash, requires the stdin to redirected from file */tmp/lkdexd* with input *ztqljsfx*

Steps to solution:
	1) Run program like in [[Embryoio Level 8]]
	2) Redirect stdin like in [[Embryoio Level 5]]

Solution:
```bash
#!/bin/bash

touch /tmp/lkdexd ; echo -ne 'ztqljsfx' > /tmp/lkdexd ; ./embryoio_level12 < /tmp/lkdexd
```

Flag:
	*pwn.college{IZfPt5qswm-ifj0_njkiXRopoOU.dJTMsQDMwUzW}*