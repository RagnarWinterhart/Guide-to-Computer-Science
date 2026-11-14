# Representing Information
Computers do not inherently understand numbers, letters, or other data everything must be translated into binary representations that the computer can then store and manipulate. 

- Binary (base 2): The number system used by computers, using only 2 digits 1s and 0s.
- Hexadecimal (base 16): A much more compact way to represent binary values, one hex digit represents 4 binary bits. Uses digits 0-9 and A-F.


To convert from hex to decimal values: 

For each number in a hex value you take its position starting at what would be the 1s position on the right and multiply it by 16 raised to the power of its position base 0.

Converting a hex number such as BAD looks something like: 
```
B = 11 in decimal
A = 10 in decimal
D = 13 in decimal

(11 x 16^2) + (10 x 16^1) + (13 x 16^0)
= (11 x 256) + (10 x 16) + (13 x 1)
= 2816 + 160 + 13 = 2989
```

Converting from binary to decimal exactly the same process except you only ever have 0s or 1s times 16^n, it can be quite tedious. 


Converting from hex to binary or vice versa just requires replacing each hex digit by the four binary bits that correspond to its value, and the other way around for the reverse operation. 


# Toy Machine
The TOY machine is a simplified computer that is based on the Von Neumann architecture, that is a model for understanding how a computer's hardware interacts to execute instructions. 

- Von Neumann Architecture: Computer architecture where program instructions and data are stored in the same memory. 

- Registers: Small and fast storage locations that are inside to processor and are used to temporarily hold values for calculations and instruction execution. 


# Machine Language Programming
Machine language programming explores how to write such low level instructions, like for TOY machines. Instead of writing code using high level programming languages, programs are written as sequences of low-level instructions for the machine. 

- Machine Language: The lowest level programming language, made of instructions that a processor can execute directly, represented numerically usually in binary or hexadecimal. 

- Memory Addresses: Instructions may reference specific places in memory to retrieve data or store it. 