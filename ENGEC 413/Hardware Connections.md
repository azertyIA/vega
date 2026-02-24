### MIPS
MIPS was developed at Stanford that is very similar to ARM and RISC-V, before it started to fall off and be good for teaching. But if you learn this, you can learn RISC V.

## Computer
A computer is a device that executes programs that YOU can make. The Von Neumann model has code instructions and data stored in memory. It's a basic cycle of fetching and executing instructions. 
- CPU performs data transformations
- Memory holds data and programs
- I/O connects input and outputs to the computer
- Buses conjoin common connections. 

A CPU (Central Processing Unit) needs to fetch instructions, decode instructions, transform data, and access memory (I/O). 
- The ALU is basically a calculator that takes in some inputs (2) and pushes an output given some instructions. 
- General Purpose Registers serve as scratch paper and are accessible by Assembly programmers. 
- Internal Registers are not accessible but help with internal counting or holding instructions.
- Internal buses connect the output of the ALU to the output register but external buses share IO or memory with the ALU. 
- Control direct data between components.

## Assembly
The goal is to go from a high-level programming language (C) to assembly and underlying hardware. You ought to know how these shits work if you're gonna write efficient, parallelizable code. 

So, let's dissect a typical C program:
```
int main(void) {
	int input[5] = {32, 100, 10, 20, 50}
	int output[5], count = 5, i;
	
	for (i = 0; i < count; i++) {
		if (input[i] >= 0) {
			output[i] = (input[i] * 9) / 5 + 32;
		}
	}
}
```
Instructions appear one per line (at most) in the following format:
- label (i.e. `loop:`) is a placeholder place in the instructions (like `goto 6` doesn't make sense)
- opcode (i.e. `BEQ`) is like the verb of the instruction
- operands (i.e. `$s0, $s1, done`) could be constants, memory locations or registers
- comments (i.e. `# i hate you so much`) are ignored by the assembler

To simply add two numbers into another, you need an ALU and 3 memory spaces. Registers go directly to the ALU with one of the inputs being selected with an immediate (constants). Typical operators are ADD, SUB, AND, OR, XOR. However x86 has a ton of bullshit parameters. In the instruction line, we should expect:
- opcode: ADD
- operands: output (reg), input 1 (reg) and input 2 (reg and not immediate)

General purpose registers are temporary storage within the CPU that are STUPID fast. They can be used to store values, addresses and intermediate values. They can be referred to by their name or number.

A register file has 4 inputs (2 read regs and 1 write regs and its value) and 2 outputs to read the read regs. For the port widths, you just need to logarithm the choices, so MIPS has 32 32-bit registers. The write operation will write on the `posedge` of the `reg_write` clock. The read is combinational though. It's more two different mechanisms of read and write.

For the registers themselves, `$0` or (`$zero`) is reserved for the value of 0, and `$31` is reserved for the return address on subroutine calls. By convention, `$8 = $t0` to `$25 = $t9` is used for temps and `$26 = $s0` to `$30 = $s3` is used for coping variables. There are two formats for ALU instructions:
1. R-Format (3 registers): `ADD`
2. I-Format (2 registers, 1 immediate): `ADDI`

The necessary steps to execute these are to fetch the content of the regs, perform the operation, and put the result back in the register file. But here's some helpful instructions:
- `LI $n, immediate # load immediate into register $n`
- `MOVE $rd, $rs # load immediate into register $n`

### Memory Declarations
In C, we need to allocate memory, assign names to memory locations, and initialize memory. For example `int A[5];` allocates 20 bytes and sets the address of the first to A. Memory looks like a linear array of cells, but its all enumerated in bytes. Memory is a bunch of boxes. There are only two types of memory access instructions in MIPS on three aligned sizes (word, half, byte):
1. `load`
2. `store`

When talking about big vs little endian means that when storing your data with words, the MSB gets stored in the LSA for big, and little endian has LSB stored in LSA and MSB gets stored in MSA.
```
.word 0x02134567
move $7, 1000
```
To write a better allocation example:
```
   .DATA
A: .WORD 0xAB
B: .WORD 0x1234
C: .WORD 0x12345678
```
These values will be bound by the assembler and the linker. 

Symbol tables are tables the chain uses to keep track of the bindings to names to values and addresses. 