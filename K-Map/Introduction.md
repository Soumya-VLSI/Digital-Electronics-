**K-MAP (KARNAUGH MAP)**

**Introduction**

- Karnaugh Map (K-Map) is a graphical method used for simplifying Boolean expressions.
- K-Map converts a truth table into a matrix-like structure and allows grouping of adjacent cells to   obtain a minimal Boolean expression.
- K-Map minimization can be performed in two forms:
- Sum of Products (SOP)
- Product of Sums (POS)

SOP and POS in K-Map

Sum of Products (SOP)
- In SOP, we consider the input combinations for which the output is HIGH (1).
- Therefore, we group cells containing `1`s.
- SOP is also called **minterm minimization**.
- SOP is represented using the notation:
F = Σm(...)

Product of Sums (POS)
*In POS, we consider the input combinations for which the output is LOW (0).
*Therefore, we group cells containing 0s.
*POS is also called maxterm minimization.
*POS is represented using the notation:
F = ΠM(...)

**RULES FOR K-MAP**

* Group should only include cells containing ones in case of SOP.
* Group should only include cells containing zeros in case of POS.
* Groups should be only horizontal or vertical.
* Groups must contain 2ⁿ cells.
* Each group should be as large as possible.
* Each cell containing one/zero(SOP/POS) must be in at least one group.
* Overlapping of groups is allowed.
* Groups can wrap around table.
* K-Map cells should be arranged in Gray Code order.
* Adjacent cells must differ in only one variable.
* Diagonal cells are not considered adjacent.
* Groups must form rectangular shapes.
* Don't-care conditions can be used for simplification.
* Don't-care cells need not be included in a group.
* Variables that change within a group are eliminated.
* Variables that remain constant determine the simplified term.
* Larger groups eliminate more variables.
* SOP groups produce product terms that are ORed together.
* POS groups produce sum terms that are ANDed together.

**K-MAP SIMPLIFICATION STEPS**
1) Write the Boolean function.
2) Determine whether SOP or POS minimization is required.
3) Draw the appropriate K-Map.
4) Arrange the variables using Gray Code.
5) Place 1s for SOP or 0s for POS.
6) Identify adjacent cells.
7) Form the largest possible groups.
8) Use overlapping or wrapping when required.
9) Ensure every required cell is covered.
10) Identify variables that remain constant.
11) Eliminate variables that change.
12) Write the simplified Boolean expression.

**2 VARIABLE K-MAP**

Truth Table

|  A  |  B  |  Minterm  |
|  0  |  0  | A'B' (m0) |
|  0  |  1  |  A'B (m1) |
|  1  |  0  |  AB' (m2) |
|  1  |  1  |   AB (m3) |

<img width="521" height="209" alt="image" src="https://github.com/user-attachments/assets/8d4b10bc-41f1-496c-95b1-50ba9a0ce059" />





