202212141106
Status: #permanent  
Tags: #linux #pwnablekr #filedescriptor

# fd
To start, the ssh shows three files available for the user. They are:
	fd
	fd.c
	flag

If I try to cat flag then I get a permission denied error, so I will have to explore an alternate avenue. Thankfully, fd.c reveals that the proper input provides the flag for us. 

In this case, the input is connected to the read function from c (description provided here "https://linuxhint.com/read-system-call-in-c/"), where the input is described as the file descriptor.

These lines are going to be the vitals ones to solving this program:
	 int fd = atoi( argv[1] ) - 0x1234; // Converts the first argument to an integer and subtracts 0x1234
     int len = 0;
     len = read(fd, buf, 32); // Reads 32 characters into buf from where the fd decides

As described in [[Managing Inputs for Payload Injection]], I need to pass $(echo -ne "some input") in order to pass for the command line.

After playing with atoi( argv[1] ), I realized that it is basically int() from Python, so I just need to pass the value of 0x1234 as the command line argument, which is 4660 as base 10.

Now that we using file descriptors to read an input from the keyboard, we need to know the right input to read. Thankfully, fd.c tells that the value is as follows:
	if(!strcmp("LETMEWIN\n", buf)){

After passing 4660 as the command line argument and typing "LETMEWIN" into stdin, you get the value:
	LETMEWIN
	good job :)
	mommy! I think I know what a file descriptor is!!

Thus the flag for pwnable.kr's first challenge is:
	mommy! I think I know what a file descriptor is!!
---
# References
