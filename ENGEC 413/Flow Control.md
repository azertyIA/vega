There are two types of flow control:
1. basic: `if` and `else`
2. iterative: `for` and `while`

All instructions are stored in memory. Each instruction is stored in 1 word or 4 bytes. Most instructions in MIPS thus increment the **program counter** (PC) by 4 for the next instruction. The only natural exception would be flow control instructions, which jump to labels instead of 4 bytes after.

On the hardware side, the PC takes the address of the next instruction using a select controlled by another ALU call to compare two registers. There are two kinds of control flow transfers:
1. unconditional: `j label`
2. conditional: `beq $t0,$t1,label` (`bne`, `bgt`, `bgeu`, `bnez` etc.)

Some examples:
```
beq $s0,$s1,label23 // if (s0 == s1) goto label23 

lw  $s0,c           // s0 = mem[&c]
li  $t0,7           // t0 = 7 (immediate)
blt $s0,$t0,label17 // if (s0 < t0) goto label17

lw  $s0,i           // s0 = mem[&i]
lw  $s1,j           // s1 = mem[&j]
bne $s0,$s1,else1   // if (s0 == s1) {
lw  $s2,f           // s2 = mem[&f]
sub $s2,$s2,$s0     // s2(f) = s2(f) - s0(i)
sw  $s2,f           // mem[&f] = s2
j   done            // } else {
else:               
lw  $s3,g           // s3 = mem[&g]
lw  $s4,h           // s4 = mem[&h]
add $s2,$s3,$s4     // s2(f) = s3(g) + s4(h)
sw  $s2,f           // mem[&f] = s2
done:               // }
```

Iterative flow control follows keeping a scratch variable in a register and changing it until a condition is met, then you just jump:
```
li   $s2,100
move $s3,$zero
la   $s4,a
la   $s5,b
looptop:
bge  $s3,$s2,done // if (s3 >= s2)
muli $t0,$s3,4
add  $t1,$t0,$s5  // B + 4 * i
add  $t2,$t0,$s4  // A + 4 * i
lw   $t3,0($t1)
sw   $t3,0($t2)   // *(A + 4 * i) = *(B + 4 * i)
addi $s3,$s3,1    // i++
j    looptop      // (turns if into while)
done:
```

```
li   $s2,100
move $s3,$zero
la   $s4,a
la   $s5,b
looptop: // eight lines with multiply
bge  $s3,$s2,done // if (s3 >= s2)
muli $t0,$s3,4
add  $t1,$t0,$s5  // B + 4 * i
add  $t2,$t0,$s4  // A + 4 * i
lw   $t3,0($t1)
sw   $t3,0($t2)   // *(A + 4 * i) = *(B + 4 * i)
addi $s3,$s3,1    // i++
j    looptop      // (turns if into while)
done:
```

```
LI   $s2,100
MOVE $s3,$zero
LA   $s4,A
LA   $s5,B
looptop: // seven lines without multiply
BGE  $s3,$s2,Done
LW   $t0,0($s5)
SW   $t0,0($s4)
ADD  $s3,$s3,1
ADD  $s5,$s5,4
ADD  $s4,$s4,4
J    LoopTop
Done:
```