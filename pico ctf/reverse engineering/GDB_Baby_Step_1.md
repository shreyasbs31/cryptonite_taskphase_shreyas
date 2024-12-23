# GDB Baby Step 1

**FLAG**: `picoCTF{549698}`


## Approach
I first installed gdb on my vm. Then i ran the command `gdb debugger0_a`. Then i used the command `info functions`, which gives 
```
0x0000000000001000  _init
0x0000000000001030  __cxa_finalize@plt
0x0000000000001040  _start
0x0000000000001070  deregister_tm_clones
0x00000000000010a0  register_tm_clones
0x00000000000010e0  __do_global_dtors_aux
0x0000000000001120  frame_dummy
0x0000000000001129  main
0x0000000000001140  __libc_csu_init
0x00000000000011b0  __libc_csu_fini
0x00000000000011b8  _fini
```
Now the challenge clearly states to look inside the main function so i disassembled the main (`disassemble main`)
```
Dump of assembler code for function main:
   0x0000000000001129 <+0>:     endbr64
   0x000000000000112d <+4>:     push   %rbp
   0x000000000000112e <+5>:     mov    %rsp,%rbp
   0x0000000000001131 <+8>:     mov    %edi,-0x4(%rbp)
   0x0000000000001134 <+11>:    mov    %rsi,-0x10(%rbp)
   0x0000000000001138 <+15>:    mov    $0x86342,%eax
   0x000000000000113d <+20>:    pop    %rbp
   0x000000000000113e <+21>:    ret
End of assembler dump.
```
Here we can clearly see that the `eax` register holds the value `0x86342`. On converting this to decimal we get our flag.
##

## What i learnt through this challenge
1. i understood GDB
##

## References
https://www.geeksforgeeks.org/gdb-step-by-step-introduction/
https://www.tutorialspoint.com/gnu_debugger/gdb_commands.htm
https://users.ece.utexas.edu/~adnan/gdb-refcard.pdf
##


#