# Linux Buffer overflow (BOF)

##Methodology

1. Investigate the file
```
file
strings
```

2. Test it out - what does the program do?

3. Look at its functions in GDB

```
info functions
```

4. Look at the assembly of a function

```
disass main
disass otherfunction
```

5. Look for the flow of the program. Look for cmp

6. Set up breakpoints with hooks

```
define hook-stop
info registers  ;show the registers
x/24xw $esp  ;show the stack
x/2i $eip  ;show the new two instructions
end
```

7. Step through the whole program. Or at the breakpoints

```
si ;steps one forward, but follows functions
ni ;does not follow functions
```

# Windows Buffer overflow (BOF)

## Links

1. Windows Exploit from scratch [https://www.nccgroup.trust/au/about-us/newsroom-and-events/blogs/2016/june/writing-exploits-for-win32-systems-from-scratch/]
2. dostackbufferoverflowgood [https://github.com/justinsteven/dostackbufferoverflowgood]
3. Buffer overflow practice [https://www.vortex.id.au/2017/05/pwkoscp-stack-buffer-overflow-practice/]
