**K-MAP (KARNAUGH MAP)**
Karnaugh Map (K-Map) is a graphical method used to simplify Boolean expressions and minimize combinational logic circuits.

What is K-Map?
A K-Map converts a Boolean function into a graphical matrix format, making it easier to identify groups of adjacent cells and obtain a simplified Boolean expression.

K-Maps are commonly used for Boolean functions with **2, 3, 4, and 5 variables**.

Types of K-Map Minimization
Sum of Products (SOP)
- Based on **minterms**
- Groups cells containing `1'
- Notation: `Σm'

Product of Sums (POS)
- Based on **maxterms**
- Groups cells containing `0'
- Notation: `ΠM'

K-Map Structure
The number of cells in a K-Map depends on the number of variables:
`Number of cells = 2ⁿ'

| Variables | Cells |
|     2     |   4   |
|     3     |   8   |
|     4     |   16  |
|     5     |   32  |

K-Map rows and columns are arranged using **Gray Code**:

`00 → 01 → 11 → 10'

This ensures that adjacent cells differ in only one variable.

Variable Elimination

The main purpose of grouping cells is to eliminate variables and obtain a simpler Boolean expression.

Larger Group
     ↓
More Variables Eliminated
     ↓
Simpler Boolean Expression
     ↓
Reduced Logic Gates
