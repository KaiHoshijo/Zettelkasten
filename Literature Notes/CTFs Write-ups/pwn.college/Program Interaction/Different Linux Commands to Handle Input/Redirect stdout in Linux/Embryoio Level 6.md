This requires the stdout to be redirected to file **mrcfqm** to get the flag.

Steps to get the flag:
	1) Run program like [[Embryoio level 1]]
	2) Redirect stdout like shown in [[Embryoio Level 5]] using command *>*

The solution is:
```bash
	touch /tmp/mrcfqm ; ./embryoio_level6 > /tmp/mrcfqm
```

The flag is:
	*pwn.college{ksPnGbq9zDXh0WxZDLgD1792J2h.0lNsQDMwUzW}*
