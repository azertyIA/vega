You need bitwise for embedded things.

Some bitwise actions that matter are:
- set (or 1)
- clear (and 0)
- invert (xor 1)
- test (all or any)

To **clear** the low order four bits for example, use:
> `ANDI $S0,$S0,0xFFFFFFF0`

To **set** specific bits 1, 3, 10, 15, 23, and 29 in a register, use:
> `ORI  $S7,$S7,0x2080840A`

To **invert** all odd bits in a register use:
> `XORI $S4,$S4,0xAAAAAAAA`

To test, you need a bit more than one instruction (this checks if all bits of a kind are set):
```
ORI  $T0,$S0,0xBFFF7FFD (set most to 1)
NOT  $T0,$T0 (turn all the ones to 0)
BEQ  $T0,$ZERO,label23 (check if any ones are left)
```
This one checks if any of the bits are set:
```
ANDI $T0,$S0,mask (leave specified)
BNE  $T0,$ZERO,label (check if any are on)
BEQ  $T0,$ZERO,label (or make sure all are off)
```

Bit shifts just move the numbers:
- shift logical: (`SLL`, `SRL`)
- shift logical by a variable amount: (`SLLV`, `SRLV`)
- shift arithmetic assumes signs: (`SLA`, `SRA` uses sign extension)

You can use these to make dynamic masks at run time (using SLLV and SRLV).