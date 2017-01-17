# ASM-Yaepl
Mimics simple assembler syntax.

- Non-OO (would translate well to simple Javascript/C)
- Modified AT&T style: ``operation source -> destination``
- Simple syntax, but still as 'cozy' as Javascript with strings, functions, etc.
- Can start with jumps/etc. for things like loops, then build up to a C-like syntax for them

# Hello, World!
```
write-line "Hello, World!" -> console //Write "Hello, World!" to the console
str-len "Hello, World!" -> $len //Store the length of "Hello, World!" as $len
int-to-str $len -> $len //Convert $len to a string before writing it
write-line $len -> console //Write $len to the console
```

# Functions
Functions could be implemented in a number of ways. Consider ``str-len`` from above:

```
@str-len $str:
    move 0 $len

    #loop
    move ($str[$len] != "\0") $continue
    move (1 + $len) $len
    jump-if $continue #loop
    
    return ($len - 1)
```

# Pros
- Syntax is extremely simple, can focus 100% on teaching the _concepts_, not the _syntax_
- 
