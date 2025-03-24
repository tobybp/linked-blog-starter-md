[[Computing]]
#16/9/24
## Numbers for Counting
- Counting uses 0, 1, 2, 3, 4,5 , 6, 7, 8, 9
- These are called **natural numbers**.
	- They are described as a set:
	- N = {0, 1, 2, 3, ... }

## Whole Numbers
- Any whole positive or negative numbers are called integers.
- The set for integer values is:
	- Z = { ... , -2, -1, 0, 1, ... }

## Rational Numbers
- Rational Numbers include values that can be shown using ratios, decimals or fractions.
- Q = { ... , 2/1. 2/2. 2/3. 2/4 ... }
- There are many more rational numbers than whole numbers.

## Irrational Numbers
- There are some numbers that cannot be expressed exactly using a fraction. We call these irrational numbers.
- The decimal values of irrational numbers are infinite, and never end.
- For example: √2 or π

## Real Numbers
- If a number is rational or irrational, it is a **real number**.
- basically any number that exists.
- This includes infinite digits like square root of 2 or pi.

## Order
- Numbers can also describe position of values.
- These values are **Ordinal Numbers**

## Binary Number System
- The binary number system uses 0 and 1 only.

## Number symbols
- The Denary system uses a combination of just ten symbols in order to represent any number.
- Number systems use a "base" to be identified. The base represent the amount of symbols that can be used to create other values.
- Decimal is base 10.
	- In decimal the number 11, for example, may be written as 11₁₀
	- In binary, it would be written as 11₂ and hexadecimal as 11₁₆

## Base 2
- Numbers using base 2 are normally referred to as binary numbers.

| Denary | Binary |
| ------ | ------ |
| 1      | 0001   |
| 2      | 0010   |
| 3      | 0011   |
| 4      | 0100   |
| 5      | 0101   |
| 6      | 0110   |
| 7      | 0111   |
| 8      | 1000   |
| 9      | 1001   |
| 10     | 1010   |
| 11     | 1011   |
| 12     | 1100   |
| 13     | 1101   |
| 14     | 1110   |
| 15     | 1111   |
## Place Value
![[Place value Computing Theory]]
10² = 100
10¹ = 10
10⁰ = 1
Therefore 253₁₀ is 2 lots of 100, 5 lots of 10, and 3 lots of 1.

Binary works in the exact same way as denary does above, but instead of using 10 to the power, it's 2.

## Hexadecimal - Base 16
- Hexadecimal uses a combination of letters and numbers in order to show values from 0 to 15.

| 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  | 11  | 12  | 13  | 14  | 15  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | A   | B   | C   | D   | E   | F   |

The place value rules also work and apply here. instead using 16 as the base.

The denary equivalent of 6E2₁₆ is:
(256 x 6) + (16 x 14) + 2 = 1,536 + 224 + 2 = 1,762₁₀

## Denary to Hex Conversion
- A much faster and simpler way to convert denary numbers into hexadecimal, is to divide by 16, then add the remainder as a second value
- e.g: 56 / 16 = 3 remainder 8
	- \= 38₁₆\

## Significance of 16
- The forth power of 2, is 16.
- Therefore base 16 numbers can be displayed using 4 bits in binary
- This allows for simple translation from binary to hex.

## Why use hex?
- Hexadecimal is much easier to read than binary.
- Hex is faster to write or type, i.e 1 character, not 4.
- Less chance of making errors when typing hex characters rather than strings of 1s and 0s.
- Very easy to convert to binary when needed.

## Conclusion
- Whole, rational, and real numbers are represented by Z, Q, and R. They are used for counting and measurement.
- Ordinal numbers are used to determine/show the position of something.
- Decimal numbers are easy to understand, but not easy to use in electronics and coding.
- Binary is simple to use with circuitry but is not easy to read as humans.
- Hexadecimal is a base that makes binary easier to read and understand.