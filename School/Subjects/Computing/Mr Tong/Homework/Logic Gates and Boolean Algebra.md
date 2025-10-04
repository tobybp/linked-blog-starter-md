[[Computing]]
#2/12/24 
## Binary Switches

- **Concept**: Electronic devices recognize current presence or absence (ON/OFF).
- **Application**: Computers use billions of switches combined to create **logic gates**

---
## Logic Gates Overview

Logic gates take one or more inputs and produce a single output, which can be used as input for subsequent gates.

### Types of Logic Gates:

1. **NOT Gate**
    - Input 0 → Output 1
    - Input 1 → Output 0

2. **AND Gate**
    - Both inputs 1 → Output 1
    - Otherwise → Output 0

3. **OR Gate**
    - Either input is 1 → Output 1
    - Otherwise → Output 0

4. **XOR (Exclusive OR) Gate**
    - One input is 1 (not both) → Output 1
    - Otherwise → Output 0

5. **NAND Gate** (NOT + AND)
    - Inverts AND output

6. **NOR Gate** (NOT + OR)
    - Inverts OR output

---
## Diagrams:
![[LOGIC GATES|300]]

---

## Boolean Algebra

1. **Basic Example**:
    - P=NOT(A AND B)P = \text{NOT}(A \text{ AND } B)P=NOT(A AND B)

2. **Combining Inputs**:
    - Boolean: P=(A⋅B)+CP = (A \cdot B) + CP=(A⋅B)+C

3. **Exclusive OR**:
    - Boolean: P=A⊕BP = A \oplus BP=A⊕B

---

## NAND – The Universal Gate

- Combines functions of NOT, OR, AND gates.
- **Advantages**:
    - Cost-effective (minimizes gate usage).
    - Increases processing speed.

