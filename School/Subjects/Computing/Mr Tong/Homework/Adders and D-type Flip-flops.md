[[Computing]]
#11/1/25

`A logic gate circuit can be used to perform the addition of two bits.`
## Half-adder
- A half adder can be used to perform the addition of two bits.
	- It takes two bits of input, A and B, then outputs the result, S and the carry, C.

| A   | B   | S   | C   |
| --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |
| 0   | 1   | 1   | 0   |
| 1   | 0   | 1   | 0   |
| 1   | 1   | 0   | 1   |

## Circuit for a half adder:
![[Half adder]]
S represents A XOR B
C represents A * B
## Limitations of half-adder
- The half adder has only two inputs so can't use the carry from previous addition for a third input.
- Can only add 1 bit numbers (0 or 1)
## Full adders
- A full adder combines two half-adders
- Has 3 inputs, A, B and carry bit C.
- Has 2 outputs, S and C

![[Full adder|600]]
- The second part of the circuit (blue) inputs the carry bit, C from a previous operation.
- The circuit outputs S and the new carry C.
#### Truth table for full adder:

| A   | B   | Cin | S   | Cout |
| --- | --- | --- | --- | ---- |
| 0   | 0   | 0   | 0   | 0    |
| 0   | 0   | 1   | 1   | 0    |
| 0   | 1   | 0   | 1   | 0    |
| 0   | 1   | 1   | 0   | 1    |
| 1   | 0   | 0   | 1   | 0    |
| 1   | 0   | 1   | 0   | 1    |
| 1   | 1   | 0   | 0   | 1    |
| 1   | 1   | 1   | 1   | 1    |
## Concatenating Full Adders
- Multiple full adders can be connected together
- `n` full adders can be connected together to input the carry bit into a subsequent adder along with two new inputs.
- Therefore the concatenated adder can be used to add two binary numbers each with `n` bits.
## Edge-triggered D-type Flip-flops
- A flip flop is an elemental sequential logic circuit that can store one bit and flip between two states, 0 and 1.
	- A D-type flip flop has one input called D, and two outputs, Q and NOT Q.
	- It also has an input of the clock signal
## The Clock
- The clock is another type of sequential circuit that changes state at regular time intervals
- A clock is needed to synchronise the change of state of flip-flop circuits.
	- An edge-triggered D-type flip-flop only changes on the rising edge of the clock's signal.
## The D-type Flip-flop as a Memory Unit
- Output Q only takes on a new value if the value at D has changed at the point of a clock pulse.
- This means that the clock pulse will freeze/store the input value at D, in Q until the next clock pulse.
![[Pasted image 20250111170450.png]]

## D-type Flip-flop
- D changes at times marked A, B, C, E, F, and G
- If D is still the same at the next clock pulse, the flip-flop will retain its current value, otherwise it will flip.
- Output Q changes at the times marked J, K, L and M:

![[Pasted image 20250111170900.png]]