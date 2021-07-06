# Assembly
![picture 2](assets/lecture8-instructionFormat.png)  

The instruction field can be of 3 types: 
- A memory-reference instruction. (MRI)
- A register or I/O instruction. (non-MRI)
- A pseudo-instruction with or without operand.

> Add I to end of MRI instructions to show that it's indirect addressing.

## Pseudo Instructions
ORG N: 
    Hex number N is the memory location for the instruction or operand listed in the following line.

END: 
    Denotes the end of symbolic program.

DEC N: 
    Signed decimal N to be converted to binary.

HEX N: 
    Hexadecimal number N to be converted to binary.
