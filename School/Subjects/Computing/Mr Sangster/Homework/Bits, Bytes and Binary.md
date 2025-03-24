[[Computing]]
#14/9/24
## Bits and Bytes:
- Computers store data using bits (binary digits: 0 and 1).
- Byte: A group of 8 bits.
- Larger data is stored by combining multiple bytes.
- Binary Representation:
- Computers process data as electrical signals, where ON = 1 and OFF = 0.
- Example: The decimal number 21 in binary is represented as 10101.
- Powers of 2:
- The number of possible combinations for n bits is  2^n .
- For example, 3 bits have  2^3 = 8  possible combinations.

## Large Data Values and Prefixes
#### Common Prefixes:
- kilo (kB) =  10^3  bytes = 1,000 bytes.
- mega (MB) =  10^6  bytes = 1,000,000 bytes.
- giga (GB) =  10^9  bytes = 1,000,000,000 bytes.
#### Base-2 Prefixes (IEC standards, introduced to avoid confusion):
- kibi (KiB) =  2^{10} = 1024  bytes.
- mebi (MiB) =  2^{20} = 1,048,576  bytes.
- gibi (GiB) =  2^{30} = 1,073,741,824  bytes.

## Representing Characters
#### ASCII:
- Developed in 1963, ASCII uses 7 bits to encode characters, giving 128 possible binary codes.
- ASCII codes represent English alphabet characters, digits, and control symbols (e.g., Enter, Backspace).
#### Unicode:
- Developed to encode characters from all languages, Unicode uses 16 or 32 bits, allowing for a much larger range of characters.
- ASCII and Unicode overlap for the first 128 characters.

## Error Detection and Correction
#### Transmission Errors:
- Data can be corrupted due to electrical interference, power surges, or synchronisation issues.
- Error Detection Techniques:
- Parity Bits: An extra bit is added to ensure the number of 1’s in a byte is even or odd.
- Majority Voting: Each bit is sent multiple times; the majority value is accepted.
- Check Digits: Used in ISBNs and credit cards, the last digit is used to verify the correctness of the preceding digits.
- Checksums: A calculated value sent with data to detect transmission errors.

## Example of Checksum Calculation (ISBN)
#### ISBN: 5014016150821
- Each digit is multiplied by a weight (alternating 1 and 3).
- Sum the results and find the remainder when divided by 10.
- Subtract the remainder from 10 to get the check digit.