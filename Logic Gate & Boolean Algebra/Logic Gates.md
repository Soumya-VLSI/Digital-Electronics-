POSITIVE AND NEGATIVE LOGIC 

Digital Circuits are called as Logic Circuit because they work on the basis of some logic. 
There are two types of logic:
1)Positive Logic 
2)Negative Logic 

In positive logic , *LOW* voltage level represents *logic 0* state and corresponding *High* voltage level represents *logic 1* state. 
0V= Logic 0 
5V= Logic 1

In negative logic, *LOW* voltage level represents *logic 1* state and corresponding *High* voltage level represents *logic 0* state.

BASIC LOGIC GATES: 

LOGIC GATE: A Logic Gate is a symbol which performs different logical operations. 

NOT GATE- A *NOT GATE* is a logic gate that inverts the digital input signal . 
It has only one input and produces it's complement.
For this reason , a *NOT GATE* is sometimes referred as an inverter. 

**Expression - Y = A'** 

<img width="280" height="211" alt="image" src="https://github.com/user-attachments/assets/bbc67c05-1048-4f97-af4c-bc97a06589ea" />

*Truth Table For NOT GATE*

|  A   |  Y = A' |
|  0   |    1    |
|  1   |    0    |

AND GATE- A *AND GATE* is a logic gate having two or more inputs and a single output . 
An AND Gate operates on logic multiplication rules. 
The AND gate gives an output 1 only when all inputs are 1.

**Expression- Y = A.B** 

<img width="343" height="199" alt="image" src="https://github.com/user-attachments/assets/da35b6de-dd24-4977-be2c-97c6c6f4e513" /> 

*Truth Table For AND Gate*

|   A   |   B   |  Y = A·B  |
|   0   |   0   |    0      |
|   0   |   1   |    0      |
|   1   |   0   |    0      |
|   1   |   1   |    1      |

OR GATE- An OR Gate is a logic gate having two or more inputs and a single output. 
An OR Gate operates on logical addition rules.
The OR gate gives an output 1 when at least one input is 1.

**Expression- Y = A + B**

<img width="377" height="173" alt="image" src="https://github.com/user-attachments/assets/ddfa99ff-1a1c-47b6-93d5-b7a55864fd12" />

*Truth Table For OR Gate*

|  A  |  B  |  Y = A+B  |
|  0  |  0  |     0     |
|  0  |  1  |     1     |
|  1  |  0  |     1     |
|  1  |  1  |     1     |

**UNIVERSAL LOGIC GATES**

A universal gate is a logic gate which can implement any Boolean function without the need to use any other type of logic gate. 
The *NAND* and *NOR* are universal logic gate.

NAND GATE- Nand Gates are gate that return false when all the inputs are true.
NAND means NOT-AND.
It is an AND gate followed by a NOT operation.

**Expression- Y = (A · B)'**

<img width="334" height="150" alt="image" src="https://github.com/user-attachments/assets/16be4ae5-2352-49b2-9e5a-4595478ef760" />

*Truth Table For NAND Gate*

|  A  |  B  |  Y  |
|  0  |  0  |  1  |
|  0  |  1  |  1  |
|  1  |  0  |  1  |
|  1  |  1  |  0  |








