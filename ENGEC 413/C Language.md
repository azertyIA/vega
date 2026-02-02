### Instruction Set Architecture
The ISA targets the hardware and the lowest level of the software. Which sucks to type in. We will start writing in assembly though because we hate ourselves. 
>It goes from portable C (compiles) to ASM (assembles) to binary objects (links) to executables (loads) to memory.

**Machine Language** is a set of operations performed by the processor and the rules for using them. The executable code is loaded from the disk and executed. **Assembly Language** turns numbers into words that are easier to look at, which the assembler turns into binaries.

C is the closest to underlying hardware than any other language we have. Maybe FORTRAN beats it... Regardless, C is about as efficient as the programmer can be. This also means its your fault for getting things wrong. A good start looks like:
```
int main(void) {
	printf("Hello World!\n");
	return 0;
}
```
The following hardware types seen in C are:
- char (byte)
- unsigned (unsigned)
- short int (halfword)
- int (word)
- long (double word)
- float (word)
- double (double word)

Declarations look like this
```
int a, b, c;
a = 20;
```
Ideally use local variables because global variables suck ass. Our base data structure is called an array. `int nums[10]` makes space for 10 uninitialized local integers in 40 local contiguous bytes in memory. Booleans don't exist so you just use zero and one. 

Some unary operators exist by using two `+` or `-` symbols but do it at different times. It's pretty cool and nonchalant. There are some good use cases. We also have if and else statements. Switch cases are also good. There's also for loops. Strings are implemented with a char array (or pointer) which terminates on a null byte.