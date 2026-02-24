Q3. The sorted array is 1234

Q5. Address zero starts at 0x10010000. Variable msg is at 0x10010010-0x10010028. Variable numbs is at 0x10010000-0x1001000f

Q6. We're overwriting the data in memory at numbs with the index of the array (decremented), as a result, numbs now stores: 4, 3, 2, 1.

Q7. 4321, 3421, 3241, 3214, 3214, 2314, 2134, 2134, 2134, 1234... until exit

Q11. 4921, 3921, 3291, 3219, 2319, 2139, 1239... until exit (something probably went sour here)

Q12. its a combination of `la` loading `msg` into the register (`$a0`) and `syscall`