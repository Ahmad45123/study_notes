# Input / Output Process
![picture 1](assets/lecture7-input_output.png)  

## Input
User is able to input data *(8 bits in basic computer)*.
When a key is stroked on the keyboard, a transmitter sends it serially into the INPR register. 

### The FGI
It's a flipflop that determines if data is available in the INPR register. The input device never puts data into the INPR register until the computer clears INPR and sets FGI back to zero.

The data is moved from the INPR register into the AC in **parallel**.

## Output
Computer is able to output characters *(8 bits in the basic computer)*.

### The FGO
It's a flipflop that, when set to zero means that the OUTR register has data in it awaiting printing. After it's printed the flipflop is set back to one and accepts new data from the AC register.

> The FGO is kind of the opposite of the FGI.

## The instructions
I/O instructions have opcode 111 and I flipflop set to one. The control signal is $D_7IT_3$. 

We will be call it $p$ for short.

#### INP
Transfer input from INPR into the first eight bits of AC(0-7). It also clears the input flag to zero.

#### OUT
Transfer data from first eight bits of AC into OUTR and clears the output flag to zero.

#### SKI/SKO
Skip the next instruction *(AKA increment PC)* if the input/output flag is set.

# Interrupts
The problem with the above is that if there's never input or output, the computer will stay stuck in an infinite loop waiting for it and not do it's normal work.

Instead of this, when either FGO or FIO are set, the PC will intterupt the computer momentarily from what it's doing to go do the transfer and then return to where it was.

The intterupt procedurce will only work if the flipflop **IEN** is set.

## The normal instruction cycle
It's the normal cycle explained before. We just make a few additions: 
- In parallel to normal operation, it checks if **IEN** is set as well as any of the two flags is set (**FGI** or **FGO**). If true, it sets a new flipflop called **R** and the next cycle will become an interrupt cycle.

$$ T_0^\prime T_1^\prime T_2^\prime (\text{IEN}) (\text{FGI} + \text{FGO}): \ R \leftarrow 1$$

- The instructions at $T_0$ to $T_2$ are modified to only work when $R$ is set to zero.

## The interrupt cycle

- The return address *(the current PC value)* is saved in memory at address 0.
- PC value is replaced with 1 and the values of IEN and R are reset.
- Location 1 in memory must be setup to branch unconditionally to I/O code.
- The last instruction in I/O code must be to indirect branch to address zero. Also ION instruction should be called.

$$ RT_0:\ AR \leftarrow 0,\ TR \leftarrow PC $$
$$ RT_1:\ M[AR] \leftarrow TR,\ PC \leftarrow 0 $$
$$ RT_2:\ PC \leftarrow PC + 1,\ IEN \leftarrow 0,\ R \leftarrow 0,\ SC \leftarrow 0 $$

# Control Logic Unit
It takes as input the decoder outputs, bits of IR, bits of AC, bits of DR and also values of the flipflops (I, S, E, R, IEN, FGI, FGI).

### Controlling registers and memory
The load, clear and increment can be controlled by scanning the list of operations and then deriving the circuit for the control.

### Controlling flipflops
We can either use JK-Flipflops or D-Flipflops. Use the excitation table to determine the equations!

#### JK Flipflop
| $Q_n$ | $Q_{n+1}$ | $J$ | $K$
| --- | --- | --- | ---
| 0 | 0 | 0 | X
| 0 | 1 | 1 | X
| 1 | 0 | X | 1
| 1 | 1 | X | 0

#### D Flipflop
| $Q_n$ | $Q_{n+1}$ | $D$
| --- | --- | ---
|0 | 0 | 0
|0 | 1 | 1
|1 | 0 | 0
|1 | 1 | 1

### Controlling the bus
It's implemented using an encoder.

![picture 1](assets/lecture7-busDecoder.png)  

The control for $x_1$, $x_2$, ..., $x_7$ are retreived from scanning the operations and making an equation for each.

### Controlling the ALU
Same as above.