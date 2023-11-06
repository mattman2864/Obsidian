A bitboard is a representation of a chessboard using multiple 64-[[bit]] numbers. it the fastest way to represent chessboards and the most commonly used among the most popular engines.
# 64-bit Number
Here is an example of what a 64-bit number looks like:
`0000000000000000000000000000000000000000000000000000000000000000`
The furthest left bit is the 63rd bit (or Most Significant Bit, abbreviated MSB), and the furthest right bit is the 0th bit (or the Least Significant Bit, abbreviated LSB). When used to represent chess state, this 64-bit number is called a bitboard.

Modern computers like the Opteron or IA64 can natively handle 64-bit numbers and manipulate them in one instruction. 32-bit computers must break up the bit operations in to 2 or more in