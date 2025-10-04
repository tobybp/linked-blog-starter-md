[[Computing]]
### Binary Addition
To look at binary addition, it may first help to look at denary addition in a different light.
The result of an addition can have a **value** and a **carry** if the result is too large to represent.

For example in 19 + 17, the first column, is 9 = 7. The result of this is 6, carry 1. Then in the next column, you have 1 + 1 + 1, which is 3. The total result is 36.

These same principles are applied to binary addition.
![[BinaryAdditionExample1|300]]
#### Adding Bytes
Computers are given a fixed number of bits to work with at a time. This can cause problems when the values exceed the number of bits given. This results in what's called an "overflow error". For example, if the computer is given 8 bits, and needs 9 to represent the result of addition.
![[BinaryAdditionExample2]]

### Binary Multiplication
Rules:
0 x 0 = 0
0 x 1 = 0
1 x 0 = 0
1 x 1 = 1

### Calculating Range
The number of bits available to use defines how many values can be represented using binary.

The highest and lowest values:
- When using unsigned, the lowest value will always be 0, and the largest number will be $2^n - 1$ where n is the number of bits available.
- When using signed, the lowest value will be $-2^{n-1}$ and the greatest value will be $2^{n-1}$ 

### Representing Negative Numbers
Two's compliment is used to represent negative numbers.
The most significant bit is switched to negative.
Instead of 128, it would be -128. 
Like an analogue counter, going back 1 from 0000 would be 1111.
The two's complement of a signed binary value is found by flipping all bits and then adding 1 to the binary.

When subtracting using twos compliment, instead of doing 43 - 17, you basically do 43 + -17. Therefore you can use the same technique as addition, in order to subtract.

### Binary Fractions
- The more bits we add to a binary value, the larger the place value of added bits become.
- Using bits to the right of the units column, mean that there are now fractional values.
- The fractional values come from negative powers of 2.
##### Fixed-point Binary
A fixed point binary value uses a specified number of bits, where the placement of the binary point is fixed.