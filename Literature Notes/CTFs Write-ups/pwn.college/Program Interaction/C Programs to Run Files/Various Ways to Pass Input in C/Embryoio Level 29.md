This program must be run in C to get the flag.

Steps to solution:
	1) Run program like in [[Embryoio level 1]]
	2) Execute a C program

Solution:
```C
#include <unistd.h>

int main() {
	return 0;
}

void pwncollege() {
	char *const args[] = {"embryoio_level29"};
	char *const envp[] = {};

	execve("./embryoio_level29", args, envp);
}
```