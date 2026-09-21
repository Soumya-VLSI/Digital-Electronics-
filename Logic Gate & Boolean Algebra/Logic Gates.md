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

**Application** 
Schmitt Inverters
Square Wave Oscillators

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

**Application**
Enable Circuitry 
Multiplier 

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

**Application**
Alarm System 

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

**Application**
Burglar Alarm 

NOR GATE- Nor Gates are gate that return false when all the inputs are true.
NOR means NOT-OR.
It is an OR gate followed by a NOT operation.

**Expression- Y = (A + B)'**

<img width="277" height="159" alt="image" src="https://github.com/user-attachments/assets/66004271-afb7-41fa-a8ad-f50f810deb0c" />

*Truth Table For NOR Gate*

|  A  |  B  |  Y  |
|  0  |  0  |  1  |
|  0  |  1  |  0  |
|  1  |  0  |  0  |
|  1  |  1  |  0  |

**Application**
Multipliers 
Half Adders and Full adders
Ripple Carry Adders 

**EXTENDED LOGIC GATE**

Extended Gates are the logical gates that has the combination of some AND,OR or NOT Gate. 

XOR GATE- The XOR takes two boolean operands and returns true of they are different. 
XOR stands for Exclusive-OR.
The XOR gate produces output 1 when the inputs are different.

**Expression**
Boolean Expression - Y = A ⊕ B
Equivalent Expression- Y = A'B + AB'

<img width="244" height="79" alt="image" src="https://github.com/user-attachments/assets/a8982d75-f51c-4b42-b97d-045eac16d1ed" />

*Truth Table For XOR Gate*

|  A  |  B  |  Y = A⊕B  |
|  0  |  0  |      0     |
|  0  |  1  |      1     |
|  1  |  0  |      1     |
|  1  |  1  |      0     |

**Application**
Addition/Subtraction
Controlled Inverter 
Parity Generator/Checker 
Check Inequality 

XOR gate produces output 1 only when inputs are not equal , it is called an anti-coincidence logic or inequality logic, also know as Odd 1’s detector.
XOR gate as an inverter- An XOR gate can be used as inverter by connecting one of two input terminal to logic 1 and feeding the input sequence to be inverted to the other terminal.   
XOR gate as a Buffer- An XOR gate can be used as inverter by connecting one of two input terminal to logic 0 and feeding the input sequence to be inverted to the other terminal.  

A xor A=0   
A xor 0=A   
A xor A'=1   
A xor 1=A'   

XNOR GATE- The XNOR Gate takes two boolean operands and returns true if they are same .
This is even Zero's Detector. 
XNOR stands for Exclusive-NOR.
The XNOR gate produces output 1 when the inputs are the same.
It is the complement of XOR.

**Expression**
Boolean Expression- Y = (A ⊕ B)'
Equivalent Expression- Y = AB + A'B'

<img width="253" height="77" alt="image" src="https://github.com/user-attachments/assets/73c96cde-6d0a-4dd9-8a55-278504a4a72b" />

*Truth Table For XNOR Gate*

|  A  |  B  |  Y  |
|  0  |  0  |  1  |
|  0  |  1  |  0  |
|  1  |  0  |  0  |
|  1  |  1  |  1  |

**Application**
Check Equality

Properties of XNOR Gate 
XNOR Gate is known as Equality detector.   
XNOR gate as an inverter- An XNOR gate can be used as inverter by connecting one of the two input terminal to logic 0 and feeding the input sequence to be inverted to the other terminal.   
XNOR gate as an Buffer- An XNOR gate can be used as buffer by connecting one of two input terminal to logic 1 and feeding the input sequence to be inverted to the other terminal.
A xnor A=1   
A xnor A'=0   
A xnor 0=A'   
A xnor 1=A  
Note: If number of input are even output will be 1   
      If numbr of inputs are odd output will be A   



