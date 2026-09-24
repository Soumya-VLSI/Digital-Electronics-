**COMBINATIONAL CIRCUITS**

Introduction

A **combinational circuit** is a digital logic circuit whose output depends only on the **present input values**.
It does not have memory or feedback.

Inputs
   ↓
Combinational Logic
   ↓
Outputs

The output can be represented as:
Output = f(Present Inputs)

**CHARACTERSTICS OF COMBINATIONAL CIRCUIT**

* Output depends only on present inputs.
* No memory element is required.
* No clock signal is required for basic operation.
* Generally does not use feedback.
* Can be described using Boolean expressions and truth tables.
* Can be implemented using logic gates.
* Can be designed and implemented using Verilog HDL.

**GENERAL STRUCTURE**

        ┌──────────────────────┐
Inputs ─►                      ├──► Outputs
        │  Combinational Logic │
        └──────────────────────┘

For 'n' input variables and 'm` output variables:

Number of possible input combinations = 2ⁿ

**MAJOR COMBINATIONAL CIRCUITS**

**Arithmetic Circuits**

* Half Adder
* Full Adder
* Half Subtractor
* Full Subtractor
* Parallel Adder
* Ripple Carry Adder
* Carry Look-Ahead Adder

**Data Selection Circuits**

* Multiplexer (MUX)
* Demultiplexer (DEMUX)

**Coding Circuits**

* Encoder
* Priority Encoder
* Decoder

**Comparison Circuits**

* Magnitude Comparator

**Important Combinational Circuits**

| Circuit          | Main Function                                     |
| ---------------- | ------------------------------------------------- |
| Half Adder       | Adds two 1-bit binary numbers                     |
| Full Adder       | Adds three 1-bit inputs including carry-in        |
| Half Subtractor  | Subtracts two 1-bit binary numbers                |
| Full Subtractor  | Performs 1-bit subtraction with borrow-in         |
| Multiplexer      | Selects one input from multiple inputs            |
| Demultiplexer    | Routes one input to one of multiple outputs       |
| Encoder          | Converts active input into coded output           |
| Priority Encoder | Encodes the highest-priority active input         |
| Decoder          | Converts coded input into one of multiple outputs |
| Comparator       | Compares two binary numbers                       |

**DESIGN APPROACH**

A typical combinational circuit can be designed using the following steps:

Problem Statement
       ↓
Identify Inputs and Outputs
       ↓
Construct Truth Table
       ↓
Derive Boolean Expression
       ↓
Simplify Boolean Expression
       ↓
Design Logic Circuit
       ↓
Implement Using Verilog
       ↓
Write Testbench
       ↓
Simulate and Verify

**VERILOG RTL IMPLEMENTATION**

Combinational circuits can be implemented in Verilog using different modeling styles.

**Common modeling styles**

* Gate-level / Structural Modeling
* Dataflow Modeling
* Behavioral Modeling

**VERIFICIATION**

Each combinational circuit can be verified using a Verilog testbench.

The testbench can:
* Apply input combinations
* Observe outputs
* Compare outputs with expected results
* Generate simulation waveforms

**Basic Verification Flow**
Design (DUT)
     ↓
Testbench
     ↓
Simulation
     ↓
Waveform
     ↓
Verify Output

**APPLICATIONS**
Combinational circuits are widely used in:
* Arithmetic Logic Units (ALUs)
* Digital signal processing systems
* Address decoding
* Control logic
* FPGA and ASIC designs
* RTL/VLSI systems


