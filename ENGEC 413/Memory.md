There are two types of variables: **static and dynamic**. However most of everything is dynamic because the runtime manager is responsible for finding the spot variables should be in memory. 

When the program gets loaded into memory, **the symbol table** updates what memory each symbol should be. If an array is being loaded, the space allocated is $size\times length$. In the context of pointers though, all addresses have the same 32-bit, 4-word size. However we only get 4 GB systems. 

> Make sure you keep memory alignment in mind! It's wasteful, but in practice very efficient.

There are two memory access instructions, they only work on aligned addresses; the `x` refers to the size of what needs to be written (`b`yte, `h`alf, `w`ord):
1. load to register: `Lx Rt, mem`
2. store to memory: `Sx Rt, mem`
- for loading bytes and halves you can implicitly convert to 2's complement without a `u`

There are also two modes to tell the computer where in memory an instruction is referring:
1. direct mode: the location is known before run time from a variable's name
	- ex: `LW $S4,VarA` (uses symbol table)
2. indirect mode: compute the address into a register and use that value to access memory
	- ex: `LW $S4,$S5`

Let's look at a code snippet (little endian):
```
lb  $t0, a # sign extend 0xAB (b) to FFFFFFAB
sb  $t0, b # push least significant AB to b
lhu $t0, f # take 0000ABCD to t0
sw  $t0, h # push 0000ABCD to h
li  $t0, 0x6789ABCD # load immediate not mem ref
```

Here's an example of C:
```
int A=0, B=7, C=8, D=27;
C = A + B + D;

   .DATA
A: .WORD  0
B: .WORD  7
C: .WORD  8
D: .WORD 23

LW  $S0, A
LW  $S1, B
LW  $S3, D
ADD $T0, $S0, $S1
ADD $S2, $T0, $S3
SW  $S2, C
```

In MIPS, indirect operands have two parts, as follows:
- `immediate(register) = immediate + register`
- the two numbers go straight from the ALU to the memory. 
- ex: `lw  $T2,12($S3)`

To actually get the inner register to add things to, you need to use the `la` instruction, which loads the address of a symbol from the symbol table. It involves an immediate to store into the register.
```
.data
A: .space 100
B: .space 100
C: .byte 5,6,7,8
D: .word 9,10,11,12
E: .space 100

la  $S0,C # $S0 <- &C
lb  $T0,0($S0) # $T0 <- MEM[&C] = 5
lb  $T0,3($S0) # $T0 <- MEM[&C + 3] = 8
la  $S1,D # $S1 <- &D
lw  $T2,4($S1) # $T0 <- MEM[&D + 4] = 10
```