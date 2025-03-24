[[Computing]]
#4/10/24 
Fixed point binary numbers have a set, pre-determined number of assigned bits for before and after the point.

This makes them easier to process, but they cannot represent the range or accuracy of the numbers that might be required to be represented.

We can hold an 8 bit number in a fixed point format such as this:

| 16  | 8   | 4   | 2   | 1   | 1/2 | 1/4 | 1/8 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |
If the number was using two's compliment, the first digit would be -16, instead of 16.
The largest number that can be held using twos compliment as shown above, is 01111111 or 15.875 in denary.

### Accuracy and Range
To store larger numbers, move the point further to the right. This increases the number of bits assigned to before the point, and reduces the bits assigned to after the point. This increases range, but decreases accuracy.
To have better precision, move the point to the left.

### Rounding Errors
When using fixed point binary numbers, you will often encounter rounding errors, where the bits cannot exactly represent the requested value. For example, if you try and represent 4.6, it would be 00100.100, but this equals 4.5, therefore there is a rounding error of 0.1

In the decimal system, 1/3 can never be represented entirely accurately. This is mirrored in the binary system, as some numbers can never be represented accurately.

### Floating Point Numbers
Numbers are stored in the format  m x 10^n when they become very large. m is known as the mantissa, and n is the exponent.

### Two's Compliment in Mantissa and Exponent
The exponent and mantissa, can use twos compliment. In normalised form, the mantissa must start with "1.0" And a negative exponent  just means that the final value will get smaller. It is the exact same as using a negative power on a number. For example, 75 x 10$^{-2}$ is 0.75.
In practice, if the exponent is negative, the binary point must be moved to the left, rather than the right.

### Normalisation
The process of moving the binary point of a floating point number to provide the maximum level of precision for a given number of bits.
We do this by ensuring that the first digit after the binary point is a significant digit.
Positive numbers always has a sign bit of 0, followed by a 1.
	This means that the mantissa of a positive number that is in a normalised form, lies between 1/2 and 1.
A non-normalised negative number will have a sign bit of 1, followed by 1 or more 1s after the binary point.
A normalised negative number has a sign bit of 1, followed by a 0 after the binary point.

### Absolute and Relative Errors
If you have an error of 2cm, in a 50cm reading, this is significant. But in a 1km reading, this is negligible. 

### Overflow
Overflow occurs when a calculation result is too big to be held in the allocated bits.
### Underflow
Underflow occurs when a calculation result is too small to be held in the allocated bits.