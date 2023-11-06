A bitboard is a representation of a chessboard using multiple 64-[[bit]] numbers. it the fastest way to represent chessboards and the most commonly used among the most popular engines.
# 64-bit Number
Here is an example of what a 64-bit number looks like:
`0000000000000000000000000000000000000000000000000000000000000000`
The furthest left bit is the 63rd bit (or Most Significant Bit, abbreviated MSB), and the furthest right bit is the 0th bit (or the Least Significant Bit, abbreviated LSB). When used to represent chess state, this 64-bit number is called a bitboard.

Modern computers like the Opteron or IA64 can natively handle 64-bit numbers and manipulate them in one instruction. 32-bit computers must break up the bit operations in to 2 or more instructions causing a slowdown of performance. However, we will be ignoring such performance issues for clarity's sake.

The operations that can happen with a 64-bit number that concern us at this moment are the logical bitwise operators: **NOT, AND, OR, XOR**. The boolean logic looks much like this:

| A   | B   | NOT A | NOT B | A AND B | A OR B | A XOR B |
| --- | --- | ----- | ----- | ------- | ------ | ------- |
| 0   | 0   | 1     | 1     | 0       | 0      | 0       |
| 0   | 1   | 1     | 0     | 0       | 1      | 1       |
| 1   | 0   | 0     | 1     | 0       | 1      | 1       |
| 1   | 1   | 0     | 0     | 1       | 1      | 0       |

In practice, this is what an AND could look like:

|     | 1010011010100110101001101010011010100110101001101010011010100110 |
| --- | ---------------------------------------------------------------- |
| AND | 0000000000111111111100000000000000000000000000000000000000000000 |
| =   | 0000000000100110101000000000000000000000000000000000000000000000                                                                 |

There are also two more operations that aren't boolean logic, but instead actions that you can perform with a 64 bit number. The LSHIFT and RSHIFT operators are left shift and right shift operators respectively. In C, LSHIFT would be `<<` and RSHIFT would be `>>`. They mean that you take the 64 bit number and shift it left or right by a specified number of bit places. If bits fall off the edge, they are gone forever and if there aren't enough bits to produce a full 64 bit number, zero are added to always keep the bits at 64. Here's an example:

Suppose we have this 64 bit number:
`1111111100000000000000000000000000000000000000000000000011111111`
If we shift it left (from LSB to MSB) by 4 bits, then this is what we end up with:
`1111000000000000000000000000000000000000000000000000111111110000`
Consequently, if we shift right by 4 bits, then this is what we get:
`0000111111110000000000000000000000000000000000000000000000001111`

Shifting might not appear to be of obvious use at the moment, but it will become very important when determining movements and attacks in parallel of certain pieces.
# FirstBit and LastBit
The function FirstBit gives the index of the first bit that is turned on from the LSB side. So in this example:
0000000000000000100000010000110000010000000010010000000100000100
FirstBit(Number) is equal to 4 which is the number of the index from zero) of the digit in the Number from the LSB side.
The function LastBit gives the index of the first bit that is turned on from the MSB side. So, continuing the above example:
LastBit(Number) is equal to 45 which is the number of the index (from zero) of the digit in the Number from the LSB side.
# [[C]] code representation
Simple C89-ish code to define a bitboard can look like this if your compiler and architecture supports the unsigned long long extension at 8 bytes width:
```c
typedef unsigned long long Birboard;
```