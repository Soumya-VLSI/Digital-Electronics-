**MULTIPLEXERS (MUX)**

1. Introduction

A **Multiplexer (MUX)** is a **combinational circuit** that selects **one input from multiple input lines** and sends the selected input to a **single output line**.

A multiplexer is also called a:

> **Data Selector**

The selection of the input is controlled by **Select Lines**.

Basic concept-
       I0 ─────┐
       I1 ─────┤
       I2 ─────┤──► MUX ───► Y
       I3 ─────┤
               │
       S1,S0 ──┘
       Select Lines
The select lines determine which input is connected to the output.

2. Why is MUX called a Data Selector?

Suppose a MUX has four inputs:
I0
I1
I2
I3
and one output:
Y
Only **one input** is selected at a time.

For example:
S1 S0 = 10
means:
Y = I2
Therefore, the MUX **selects one data input and forwards it to the output**.

3. Basic Structure of a MUX

A MUX consists of:

* Data inputs
* Select lines
* One output

For a MUX having `n` select lines:

Number of inputs = 2^n
Number of outputs = 1

Examples

| Select Lines | Data Inputs | Output |
|       1      |      2      |    1   |
|       2      |      4      |    1   |
|       3      |      8      |    1   |
|       4      |     16      |    1   |

Therefore:

2:1 MUX → 1 select line
4:1 MUX → 2 select lines
8:1 MUX → 3 select lines
16:1 MUX → 4 select lines

4. 2:1 Multiplexer

A **2:1 MUX** has:

* 2 data inputs
* 1 select line
* 1 output

        I0 ─────┐
                │
                │
        I1 ─────┤──► MUX ───► Y
                │
        S ──────┘

Inputs: I0, I1
Select line: S
Output: Y

5. Truth Table of 2:1 MUX

|  S  |  Y  |
|  0  |  I0 |
|  1  |  I1 |

When:
S = 0
the output is:
Y = I0
When:
S = 1
the output is:
Y = I1
Therefore:

> `S` decides which input reaches the output.

6. Boolean Expression of 2:1 MUX

The Boolean expression is:
Y = S'I0 + SI1

Understanding the expression

First term:
S'I0
works when:
S = 0
Second term:
SI1
works when:
S = 1
Therefore:
Y = S'I0 + SI1

7. Logic Implementation of 2:1 MUX

A 2:1 MUX can be implemented using:

* 1 NOT gate
* 2 AND gates
* 1 OR gate
             ┌── NOT ──┐
             │         │
             S         S'
             │         │
I0 ───────── AND ──────┐
                       │
I1 ───────── AND ──────┤── OR ──► Y
             │         │
             S         │

The output equation is:
Y = S'I0 + SI1

8. 4:1 Multiplexer

A **4:1 MUX** has:

* 4 data inputs
* 2 select lines
* 1 output

Inputs:
I0, I1, I2, I3
Select lines:
S1, S0
Output:
Y

Basic representation:

 I0 ─────┐
 I1 ─────┤
 I2 ─────┤──► 4:1 MUX ───► Y
 I3 ─────┤
         │
 S1,S0 ──┘

9. Truth Table of 4:1 MUX

|  S1  |  S0  | Output |
|  0   |   0  |   I0   |
|  0   |   1  |   I1   |
|  1   |   0  |   I2   |
|  1   |   1  |   I3   |

Selection
S1 S0 = 00 → Y = I0
S1 S0 = 01 → Y = I1
S1 S0 = 10 → Y = I2
S1 S0 = 11 → Y = I3

10. Boolean Expression of 4:1 MUX

The Boolean expression is:

Y = S1'S0'I0
  + S1'S0I1
  + S1S0'I2
  + S1S0I3

Each input has a corresponding **select-line combination**.

| Select Combination | Selected Input |
|       S1'S0'       |      I0        |
|       S1'S0        |      I1        |
|       S1S0'        |      I2        |
|       S1S0         |      I3        |


11. 8:1 Multiplexer

An **8:1 MUX** has:

* 8 data inputs
* 3 select lines
* 1 output

Inputs:
I0, I1, I2, I3, I4, I5, I6, I7

Select lines:
S2, S1, S0

Output:
Y

12. Truth Table of 8:1 MUX

|12. Truth Table of 8:1 MUX
S2	S1	S0	Output
0	0	0	I0
0	0	1	I1
0	1	0	I2
0	1	1	I3
1	0	0	I4
1	0	1	I5
1	1	0	I6
1	1	1	I7

Therefore:

000 → I0
001 → I1
010 → I2
011 → I3
100 → I4
101 → I5
110 → I6
111 → I7
13. Boolean Expression of 8:1 MUX

The output can be written as:

Y = S2'S1'S0'I0
  + S2'S1'S0I1
  + S2'S1S0'I2
  + S2'S1S0I3
  + S2S1'S0'I4
  + S2S1'S0I5
  + S2S1S0'I6
  + S2S1S0I7
14. 16:1 Multiplexer

A 16:1 MUX has:

16 data inputs
4 select lines
1 output

Inputs:

I0, I1, I2, I3, I4, I5, I6, I7,
I8, I9, I10, I11, I12, I13, I14, I15

Select lines:

S3, S2, S1, S0

Output:

Y
15. Truth Table of 16:1 MUX
S3	S2	S1	S0	Output
0	0	0	0	I0
0	0	0	1	I1
0	0	1	0	I2
0	0	1	1	I3
0	1	0	0	I4
0	1	0	1	I5
0	1	1	0	I6
0	1	1	1	I7
1	0	0	0	I8
1	0	0	1	I9
1	0	1	0	I10
1	0	1	1	I11
1	1	0	0	I12
1	1	0	1	I13
1	1	1	0	I14
1	1	1	1	I15
16. General MUX Formula

For a MUX having 2^n inputs:

Number of data inputs = 2^n
Number of select lines = n
Number of outputs = 1

Examples:

2^1 = 2  → 2:1 MUX
2^2 = 4  → 4:1 MUX
2^3 = 8  → 8:1 MUX
2^4 = 16 → 16:1 MUX
17. MUX Using Smaller MUXes

Larger multiplexers can be constructed using smaller multiplexers.

For example:

4:1 MUX using 2:1 MUXes

Three 2:1 MUXes are required.

        I0 ──┐
             ├── 2:1 ──┐
        I1 ──┘         │
                       ├── 2:1 ──► Y
        I2 ──┐         │
             ├── 2:1 ──┘
        I3 ──┘

        S0 controls first two MUXes
        S1 controls final MUX

Number of 2:1 MUXes required:

4:1 MUX = 3 × 2:1 MUX
18. 8:1 MUX Using 2:1 MUXes

An 8:1 MUX can be constructed using:

7 × 2:1 MUXes

Structure:

Level 1 → 4 MUXes
Level 2 → 2 MUXes
Level 3 → 1 MUX

Total = 4 + 2 + 1 = 7

General formula:

Number of 2:1 MUXes required
= 2^n - 1

For an 8:1 MUX:

2^3 - 1 = 7
19. MUX as a Universal Logic Function Generator

A MUX can be used to implement Boolean functions.

For example, a Boolean function can be implemented by connecting:

Variables to select lines
Logic constants or other variables to data inputs

Possible data inputs can be:

0
1
A
A'
B
B'

depending on the required function.

This makes MUX an important circuit for digital logic implementation.

20. MUX Applications

Multiplexers are used in many digital systems.

1. Data Selection

Selecting one data source from multiple sources.

2. Data Routing

Routing data from different sources to a common destination.

3. Communication Systems

Selecting different signals or channels.

4. Processor and ALU Design

Selecting operands and different data paths.

5. Control Systems

Selecting different control signals.

6. Digital Systems

Reducing the number of physical connections.

7. Parallel Data Selection

Selecting one of several parallel data lines.

21. Advantages of MUX
Reduces the number of required connections.
Allows multiple data sources to share one output.
Useful for data routing.
Can implement Boolean functions.
Reduces hardware in many digital systems.
Simple and efficient data-selection mechanism.
22. Limitations of MUX
Only one input can normally be selected at a time.
Larger MUXes require more hardware.
Propagation delay increases as the MUX structure becomes larger.
Select-line control is required.
23. MUX vs DEMUX
Feature	MUX	DEMUX
Full form	Multiplexer	Demultiplexer
Function	Many inputs → One output	One input → Many outputs
Also called	Data Selector	Data Distributor
Data Inputs	Multiple	One
Outputs	One	Multiple
Select lines	Used for input selection	Used for output selection
Easy way to remember
MUX:
Many → One

DEMUX:
One → Many
24. MUX vs Encoder

These two circuits are different.

MUX
Many data inputs
       ↓
      MUX
       ↓
One output
Encoder
One active input
       ↓
    Encoder
       ↓
Binary code

A MUX selects data, whereas an encoder converts an active input into a binary code.

25. MUX vs Decoder
MUX
Many inputs → One output
Decoder
Binary input → One of many outputs

A decoder activates an output according to the binary input combination.

