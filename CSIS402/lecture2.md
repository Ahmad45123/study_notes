# Memory
- Stores information in form of groups of bytes called **words**.
- Data is read and written in terms of words and not single bits or bytes.
- Number of address lines is $log_2(\text{No. Of Words})$
- Number of data lines is equal to the word size.
- Maximum number of bytes = Number of bits divided by 8.

## RAM
- Main memory of computer system.
- Volatine. Data is lost when power is lost.
- Very fast and access location via address lines.

![picture 1](assets/lecture2-ram.png)  

## ROM
- Doesn't have write capability.

![picture 2](assets/lecture2-rom.png)  

# Arthmetic Micro-Operations

## 1-bit Adder
![picture 3](assets/lecture2-1bit-adder.png)  

We can connect 1-bit adders together to make n-bit addition.

### Negative Numbers
In order to get the negative of a number we apply 2's complement.

$$ \bar{R} +1 $$

### Adder/Subtracter Circuit
![picture 4](assets/lecture2-adder-subtracter.png)  

If control has value of $0$, it works as adder. If control is $1$, it's a subtracter.
