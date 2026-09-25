# Multiplexers (MUX)

## 1. Introduction

A **Multiplexer (MUX)** is a **combinational circuit** that selects **one input from multiple input lines** and sends the selected input to a **single output line**.

A multiplexer is also called a:

> **Data Selector**

The selection of the input is controlled by **Select Lines**.

### Basic concept

```text
       I0 ─────┐
       I1 ─────┤
       I2 ─────┤──► MUX ───► Y
       I3 ─────┤
               │
       S1,S0 ──┘
       Select Lines
```

The select lines determine which input is connected to the output.

---

# 2. Why is MUX called a Data Selector?

Suppose a MUX has four inputs:

```text
I0
I1
I2
I3
```

and one output:

```text
Y
```

Only **one input** is selected at a time.

For example:

```text
S1 S0 = 10
```

means:

```text
Y = I2
```

Therefore, the MUX **selects one data input and forwards it to the output**.

---

# 3. Basic Structure of a MUX

A MUX consists of:

* Data inputs
* Select lines
* One output

For a MUX having `n` select lines:

### Number of inputs

```text
Number of inputs = 2^n
```

### Number of outputs

```text
Number of outputs = 1
```

### Examples

| Select Lines | Data Inputs | Output |
| -----------: | ----------: | -----: |
|            1 |           2 |      1 |
|            2 |           4 |      1 |
|            3 |           8 |      1 |
|            4 |          16 |      1 |

Therefore:

```text
2:1 MUX → 1 select line
4:1 MUX → 2 select lines
8:1 MUX → 3 select lines
16:1 MUX → 4 select lines
```

---

# 4. 2:1 Multiplexer

A **2:1 MUX** has:

* 2 data inputs
* 1 select line
* 1 output

```text
        I0 ─────┐
                │
                │
        I1 ─────┤──► MUX ───► Y
                │
        S ──────┘
```

Inputs:

```text
I0, I1
```

Select line:

```text
S
```

Output:

```text
Y
```

---

## 5. Truth Table of 2:1 MUX

| S | Y  |
| - | -- |
| 0 | I0 |
| 1 | I1 |

### Working

When:

```text
S = 0
```

the output is:

```text
Y = I0
```

When:

```text
S = 1
```

the output is:

```text
Y = I1
```

Therefore:

> `S` decides which input reaches the output.

---

# 6. Boolean Expression of 2:1 MUX

The Boolean expression is:

```text
Y = S'I0 + SI1
```

### Understanding the expression

First term:

```text
S'I0
```

works when:

```text
S = 0
```

Second term:

```text
SI1
```

works when:

```text
S = 1
```

Therefore:

```text
Y = S'I0 + SI1
```

---

# 7. Logic Implementation of 2:1 MUX

A 2:1 MUX can be implemented using:

* 1 NOT gate
* 2 AND gates
* 1 OR gate

```text
             ┌── NOT ──┐
             │         │
             S         S'
             │         │
I0 ───────── AND ──────┐
                       │
I1 ───────── AND ──────┤── OR ──► Y
             │         │
             S         │
                       │
```

The output equation is:

```text
Y = S'I0 + SI1
```

---

# 8. 4:1 Multiplexer

A **4:1 MUX** has:

* 4 data inputs
* 2 select lines
* 1 output

Inputs:

```text
I0, I1, I2, I3
```

Select lines:

```text
S1, S0
```

Output:

```text
Y
```

Basic representation:

```text
 I0 ─────┐
 I1 ─────┤
 I2 ─────┤──► 4:1 MUX ───► Y
 I3 ─────┤
         │
 S1,S0 ──┘
```

---

# 9. Truth Table of 4:1 MUX

| S1 | S0 | Output |
| -- | -- | ------ |
| 0  | 0  | I0     |
| 0  | 1  | I1     |
| 1  | 0  | I2     |
| 1  | 1  | I3     |

### Selection

```text
S1 S0 = 00 → Y = I0
S1 S0 = 01 → Y = I1
S1 S0 = 10 → Y = I2
S1 S0 = 11 → Y = I3
```

---

# 10. Boolean Expression of 4:1 MUX

The Boolean expression is:

```text
Y = S1'S0'I0
  + S1'S0I1
  + S1S0'I2
  + S1S0I3
```

Each input has a corresponding **select-line combination**.

| Select Combination | Selected Input |
| ------------------ | -------------- |
| S1'S0'             | I0             |
| S1'S0              | I1             |
| S1S0'              | I2             |
| S1S0               | I3             |

---

# 11. 8:1 Multiplexer

An **8:1 MUX** has:

* 8 data inputs
* 3 select lines
* 1 output

Inputs:

```text
I0, I1, I2, I3, I4, I5, I6, I7
```

Select lines:

```text
S2, S1, S0
```

Output:

```text
Y
```

---

## 12. Truth Table of 8:1 MUX

|

