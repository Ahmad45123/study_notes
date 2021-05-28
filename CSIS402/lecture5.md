# Instruction Format
It's always 16 bits long.
## Memory Reference Format
- Addressing Mode bit is first.
- 3 Opcode bits ranging from $000$ to $110$.
- Address bits. (12)

## Register Reference Format
- Addressing bit is ALWAYS zero.
- Opcode is $111$ meaning it's register OR operations on I/O.
- No address is needed so the 12 bits are used to specify the operation on the $\text{AC}$ register.

## I/O Format
- Addressing bit is ALWAYS one.
- Opcode is also $111$.
- 12 bits specify the type of IO operation.

# Control
- The whole system is driven by a common clock.
- Registers only change their values on a clock pulse if the respective load is enabled.
- Control could be hardwired, thus the control logic is implemented via gates, decodes, flip-flops, etc.
- Control could also be mircoprogrammed, thus any changes in logic require changes in code only.
- When looking at a rising edge in a clock, we look directly behind it to know if signal is on or off.