**ARITHEMATIC CIRCUITS**

**Arithmetic circuits** are combinational digital circuits used to perform mathematical operations on binary numbers.

They are important building blocks of digital systems such as:

* Arithmetic Logic Units (ALUs)
* Processors
* Digital signal processors
* Calculators
* Microcontrollers
* FPGA and ASIC designs
* VLSI systems

Since arithmetic circuits are **combinational circuits**, their outputs depend only on the **present input values**.

**Types of Arithmetic Circuits**

The important arithmetic circuits are:

Arithmetic Circuits
        │
        ├── Adders
        │   ├── Half Adder
        │   ├── Full Adder
        │   ├── Parallel Adder
        │   ├── Ripple Carry Adder
        │   └── Carry Look-Ahead Adder
        │
        └── Subtractors
            ├── Half Subtractor
            └── Full Subtractor

**HALF ADDER**

A **Half Adder** is a combinational circuit that adds two 1-bit binary numbers.

Inputs- A, B
Outputs- Sum (S)
       - Carry (C)

Boolean Expressions
S = A ⊕ B
C = A · B

Truth Table

|  A  |  B  |  Sum  |  Carry  |
|  0  |  0  |   0   |   0     |
|  0  |  1  |   1   |   0     |
|  1  |  0  |   1   |   0     |
|  1  |  1  |   0   |   1     |

Logic Implementation
Sum   → XOR gate
Carry → AND gate

Limitation

A Half Adder does **not** have a Carry-in input.

Therefore, it cannot directly add three bits.

4. Full Adder

A **Full Adder** is a combinational circuit that adds three 1-bit inputs.

Inputs
A
B
Cin → Carry-in

Outputs
Sum
Cout → Carry-out

Boolean Expressions
Sum = A ⊕ B ⊕ Cin
Cout = AB + BCin + ACin

Another commonly used form:
Cout = AB + Cin(A ⊕ B)

Truth Table

| A | B | Cin | Sum | Cout |
| 0 | 0 | 0   | 0   | 0    |
| 0 | 0 | 1   | 1   | 0    |
| 0 | 1 | 0   | 1   | 0    |
| 0 | 1 | 1   | 0   | 1    |
| 1 | 0 | 0   | 1   | 0    |
| 1 | 0 | 1   | 0   | 1    |
| 1 | 1 | 0   | 0   | 1    |
| 1 | 1 | 1   | 1   | 1    |

Important Point

A Full Adder can be constructed using:
2 Half Adders + 1 OR Gate

5. Half Subtractor
A **Half Subtractor** performs subtraction of two 1-bit binary numbers.

Inputs
A → Minuend
B → Subtrahend
Outputs
Difference (D)
Borrow (Bout)

Boolean Expressions
D = A ⊕ B
Bout = A'B

Truth Table

| A | B | Difference | Borrow |
| - | - | ---------- | ------ |
| 0 | 0 | 0          | 0      |
| 0 | 1 | 1          | 1      |
| 1 | 0 | 1          | 0      |
| 1 | 1 | 0          | 0      |

### Important Point

A Half Subtractor does not have a **Borrow-in** input.

---

# 6. Full Subtractor

A **Full Subtractor** performs subtraction of three 1-bit inputs.

### Inputs

```text
A
B
Bin → Borrow-in
```

### Outputs

```text
Difference
Bout → Borrow-out
```

### Boolean Expressions

```text
Difference = A ⊕ B ⊕ Bin
```

```text
Bout = A'B + A'Bin + BBin
```

### Truth Table

| A | B | Bin | Difference | Bout |
| - | - | --- | ---------- | ---- |
| 0 | 0 | 0   | 0          | 0    |
| 0 | 0 | 1   | 1          | 1    |
| 0 | 1 | 0   | 1          | 1    |
| 0 | 1 | 1   | 0          | 1    |
| 1 | 0 | 0   | 1          | 0    |
| 1 | 0 | 1   | 0          | 0    |
| 1 | 1 | 0   | 0          | 0    |
| 1 | 1 | 1   | 1          | 1    |

---

# 7. Parallel Adder

A **Parallel Adder** is used to add two multi-bit binary numbers.

Multiple Full Adders are connected together to perform the addition of multiple bits simultaneously.

For an `n-bit` parallel adder:

```text
Number of Full Adders = n
```

Example for 4-bit addition:

A3 A2 A1 A0
+ B3 B2 B1 B0
--------------
C4 S3 S2 S1 S0

Four Full Adders are required.

8. Ripple Carry Adder

A **Ripple Carry Adder (RCA)** is a multi-bit binary adder constructed by connecting Full Adders in cascade.

The carry output of one Full Adder becomes the carry input of the next Full Adder.

        C0
         │
         ▼
      ┌─────┐
A0 ──►│ FA0 │──► C1
B0 ──►│     │
      └──┬──┘
         │ S0

         C1
         │
         ▼
      ┌─────┐
A1 ──►│ FA1 │──► C2
B1 ──►│     │
      └──┬──┘
         │ S1


### Main disadvantage

The carry must propagate from one Full Adder to the next.

Therefore, the propagation delay increases as the number of bits increases.

# 9. Carry Look-Ahead Adder

A **Carry Look-Ahead Adder (CLA)** is designed to reduce the carry propagation delay found in Ripple Carry Adders.

Instead of waiting for the carry to ripple through each Full Adder, the CLA calculates carries using **Generate** and **Propagate** concepts.

A carry is generated when:

Gi = AiBi

Propagate

A common definition is:
Pi = Ai ⊕ Bi

The carry equation is:

Ci+1 = Gi + PiCi

Therefore, the carry can be calculated more quickly.

Main advantage

**Lower carry propagation delay compared with a Ripple Carry Adder.**

10. Adder Comparison

| Circuit                | Inputs    | Main Purpose              |
| ---------------------- | --------- | ------------------------- |
| Half Adder             | A, B      | Adds 2 bits               |
| Full Adder             | A, B, Cin | Adds 3 bits               |
| Parallel Adder         | Multi-bit | Adds multi-bit numbers    |
| Ripple Carry Adder     | Multi-bit | Simple multi-bit addition |
| Carry Look-Ahead Adder | Multi-bit | Faster multi-bit addition |

11. Adder vs Subtractor

| Feature       | Adder           | Subtractor           |
| ------------- | --------------- | -------------------- |
| Operation     | Addition        | Subtraction          |
| Output        | Sum, Carry      | Difference, Borrow   |
| Basic circuit | Half/Full Adder | Half/Full Subtractor |
| Carry         | Used            | Borrow is used       |

**APPLICATIONS**
Arithmetic circuits are used in:
* Microcontrollers
* Digital signal processors
* Counters
* Arithmetic operations
* Digital calculators
* FPGA and ASIC designs
* VLSI systems
