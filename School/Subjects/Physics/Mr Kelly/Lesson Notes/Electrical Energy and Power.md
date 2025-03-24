[[Physics]]
#7/10/24
### Energy
- Energy is equal to the work done.
- When a 1A current flows across a 1V potential difference for 1 second, 1 Joule is transformed electrically
### Power
- Power is the rate at which work is done.
- When a 1A current flows across a 1V potential difference for 1 second, a power of 1 Watt is developed

## Electromagnetic force (_emf_) and the Volt

Electromagnetic force, or _emf_, is a term used to describe the work done on the charges bt a cell or power supply.
_emf_ is the work done per unit charge when chemical energy is transformed into electrical energy.

Examples of _emf_ sources are cell, solar cell, thermocouple, and dynamo

The equation for calculating _emf_ is:

# <span style="color:rgb(150, 200, 255)">ε = W/Q</span>
Where ε is the _emf_
W is the work done (energy transferred)
Q is the charge

# Calculating work done or energy transferred
We have W = QV = Qε and previously Q = It

Setup the circuit as shown
Take readings of current and p.d, then calculate the work done by the resistor.
Swap the resistor for the other values and repeat, recording your results in a suitable table.

![[workdoneenergytransferredpractical|600]]

| Resistance | Current | Potential Difference | Charge 1s | Charge 5s | Charge 10s | Work Done 1s | Work Done 5s | Work Done 10s |
| ---------- | ------- | -------------------- | --------- | --------- | ---------- | ------------ | ------------ | ------------- |
| 1Ω         | 1.062   | 1.07                 | 1.062     | 5.31      | 10.62      | 1.13634      | 5.6817       | 11.3634       |
| 6.8Ω       | 0.312   | 2.11                 | 0.312     | 1.56      | 3.12       | 0.65832      | 3.2916       | 6.5832        |
| 10Ω        | 0.227   | 2.24                 | 0.227     | 1.135     | 2.27       | 0.50848      | 2.5424       | 5.0848        |
| 22Ω        | 0.110   | 2.40                 | 0.110     | 0.550     | 1.10       | 0.264        | 1.32         | 2.64          |
| 47Ω        | 0.052   | 2.49                 | 0.052     | 0.26      | 0.52       | 0.12948      | 0.6474       | 1.2948        |

### Conclusion:
As the resistance of the resistor increases, the current decreases, and the potential difference increases, due to it being more difficult to get energy through the resistor, therefore it must have a high energy per unit charge.
As the resistance increases, the work done decreases. 

## Calculating Electrical Energy

<span style="color:rgb(150, 200, 255)">Electrical Energy = Current x potential Difference x Time</span>
## <span style="color:rgb(150, 200, 255)">E = I x V x t</span>

## Calculating Electrical Power

<span style="color:rgb(150, 200, 255)">Electrical power = Current x Potential Difference</span>
P = Electrical energy / Time
P = E / t
P = I x V

We can abreviate the power formula to P = I x V <span style="color:rgb(255, 200, 100)">...... eqn1</span>
We know from Ohm's law that V = I x R <span style="color:rgb(255, 200, 100)">...... eqn2</span>

Substituting <span style="color:rgb(255, 200, 100)">eqn2</span> into <span style="color:rgb(255, 200, 100)">eqn1</span> gives:
P = I x V = I x I x R = I$^2$ x R <span style="color:rgb(255, 200, 100)">...... eqn3</span>

Substituting V/R for i in <span style="color:rgb(255, 200, 100)">eqn1</span> gives us:
P = I x V = V/R x V = V$^2$ / R <span style="color:rgb(255, 200, 100)">...... eqn4</span>

For example on the 1Ω resistors readings:
#### Using <span style="color:rgb(255, 200, 100)">eqn3</span> in place of <span style="color:rgb(255, 200, 100)">eqn1</span>:
P = I x V = I x I x R = I$^2$ x R
\= 1.062$^2$ x 1
\= 1.127844
Very similar to the 1.13634 result from <span style="color:rgb(255, 200, 100)">eqn1</span>.

\= 0.227$^2$ x 10
\= 0.051529 x 10
\= 0.51529
Very similar to the 0.50848 result from <span style="color:rgb(255, 200, 100)">eqn1</span>.
#### Using <span style="color:rgb(255, 200, 100)">eqn4</span> in place of <span style="color:rgb(255, 200, 100)">eqn1</span>::
Current = 1.062
Potential Difference = 1.07
V$^2$ / R = 1.07$^2$ / 1 
\= 1.1449
Very close to the 1.13634 result from <span style="color:rgb(255, 200, 100)">eqn1</span>.
