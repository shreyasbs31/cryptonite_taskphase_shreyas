# ARMssembly1

### Flag
the flag is ``` picoCTF{0000004d} ```
###

### Thought Process
the given file contained assembly code and we had to find the argument for which the code would run the 'win' condition.

```
func:
	sub	sp, sp, #32
	str	w0, [sp, 12]
	mov	w0, 58
	str	w0, [sp, 16]
	mov	w0, 2
	str	w0, [sp, 20]
	mov	w0, 3
	str	w0, [sp, 24]
	ldr	w0, [sp, 20]
	ldr	w1, [sp, 16]
	lsl	w0, w1, w0
	str	w0, [sp, 28]
	ldr	w1, [sp, 28]
	ldr	w0, [sp, 24]
	sdiv	w0, w1, w0
	str	w0, [sp, 28]
	ldr	w1, [sp, 28]
	ldr	w0, [sp, 12]
	sub	w0, w1, w0
	str	w0, [sp, 28]
	ldr	w0, [sp, 28]
	add	sp, sp, 32
```

This was the function. 
the first line creates a stack of 32 bytes.
then the function stores the values 58, 2, 3.
then it loads the value of w0 as 2 and w1 as 58 and then performs bitwise operation (left shifts w1 by w0 or left shifts 58 by 2 which means 58*4=232) and then stores that result in w0.

next, we load w1 as 232 and w0 as 3, and then divide w1 by w0 and store that value in w0 (which is 77)
Now you load w1 as the previous value obtained which is 77 and then free up the stack space.

Now to achieve the win condition, the expression should be compared to 0, so 77-value = 0, so the argument required to win is 77, which in hex is 0000004d.
###

### What i learnt through this challene
how to read assembly code and understand the syntaxes and what stack pointers are.
###

### References
https://www.youtube.com/watch?v=1d-6Hv1c39c
###

#