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

**K-MAP GRAPHICAL METHOD**
To minimise the cicruit 
n= no. of variables 
2^n= no. of box k-map must have 
n = 2 = 4box
n = 3 = 8box
n = 4 = 16box

**2 VARIABLE K-MAP**

Truth Table

|  A  |  B  |  Minterm  |
|  0  |  0  | A'B' (m0) |
|  0  |  1  |  A'B (m1) |
|  1  |  0  |  AB' (m2) |
|  1  |  1  |   AB (m3) |

<img width="521" height="209" alt="image" src="https://github.com/user-attachments/assets/8d4b10bc-41f1-496c-95b1-50ba9a0ce059" />

**3 VARIABLE K-MAP**

Truth Table

A | B | C | Min Term
0 | 0 | 0 | A'B'C' (m0)
0 | 0 | 1 | A'B'C (m1)
0 | 1 | 0 | A'BC' (m2)
0 | 1 | 1 | A'BC (m3)
1 | 0 | 0 | AB'C' (m4)
1 | 0 | 1 | AB'C (m5)
1 | 1 | 0 | ABC' (m6)
1 | 1 | 1 | ABC (m7)

<img width="541" height="286" alt="image" src="https://github.com/user-attachments/assets/1efed494-3221-46a0-889f-673a655c8045" />

**4 VARIABLE K-MAP**

Truth Table 

A | B | C | D |    Min Term   |
0 | 0 | 0 | 0 |  A'B'C'D' (m0)|
0 | 0 | 0 | 1 |  A'B'C'D (m1) | 
0 | 0 | 1 | 0 |  A'B'CD' (m2) |
0 | 0 | 1 | 1 |  A'B'CD (m3)  |
0 | 1 | 0 | 0 |  A'BC'D' (m4) |
0 | 1 | 0 | 1 |  A'BC'D (m5)  | 
0 | 1 | 1 | 0 |  A'BCD' (m6)  |
0 | 1 | 1 | 1 |  A'BCD (m7)   |
1 | 0 | 0 | 0 |  AB'C'D' (m8) |
1 | 0 | 0 | 1 |  AB'C'D (m9)  |
1 | 0 | 1 | 0 |  AB'CD' (m10) |
1 | 0 | 1 | 1 |  AB'CD (m11)  |
1 | 1 | 0 | 0 |  ABC'D' (m12) |
1 | 1 | 0 | 1 |  ABC'D (m13)  |
1 | 1 | 1 | 0 |  ABCD' (m14)  |
1 | 1 | 1 | 1 |  ABCD (m15)   |

https://www.geeksforgeeks.org/what-is-minterm/<img width="541" height="286" alt="image" src="https://github.com/user-attachments/assets/909e7f93-d8a5-4201-adc6-b97e560123b1" />

**Note-**If all values are 1 then it is logic 1 
If 1 is found in two or more groups then it is said to be the redundant block with the help of redundancy theorem. 

For POS we consider the 0 and we write 0 at place of 1.

**K-MAP DON'T CARE**
In some digital circuits, certain input combinations never occur or the output for those combinations does not matter.
Such input combinations are called Don't-Care conditions.
They are represented by: X or d

Don't-care conditions are used during K-Map minimization to obtain a simpler Boolean expression.

**Why Do Don't-Care Conditions Occur?**
Don't-care conditions commonly occur when:
Some input combinations are invalid.
Some input combinations never occur in normal operation.
Certain input combinations are unused.
The output is irrelevant for particular input combinations.

Representation of Don't-Care Conditions
Don't-care conditions are usually represented using:
X or using minterm notation:
d(...)
Example
Y = Σm(1,3,7) + d(5,6)

Here:

Σm(1,3,7) → Required 1s
d(5,6)    → Don't-care conditions

Don't-Care in K-Map
In a K-Map, don't-care cells are marked as: X

Example:

       BC
       00  01  11  10
     +---+---+---+---+
 A 0 | 1 | X | 1 | 0 |
     +---+---+---+---+
 A 1 | 0 | 1 | X | 0 |
     +---+---+---+---+

The X cells can be used to create larger groups if they help simplify the expression.

**Most Important Rule**

A don't-care can be treated as either:
1 or 0 depending on which choice gives a simpler Boolean expression.
Therefore:
Don't-care = 1 → if it helps grouping
Don't-care = 0 → if it does not help grouping

**Don't-Care in SOP Minimization**
For SOP minimization:
Group 1s
Don't-care X cells may be included in the group.

Example
Y = Σm(1,3,7) + d(5)
The X at minterm 5 can be included if it helps create a larger group.
The goal is to obtain the simplest SOP expression.

**Don't-Care in POS Minimization**
For POS minimization:
Group 0s
Don't-care X cells may be treated as 0 when doing so helps create a larger group.
Remember : 
Minimization	Group	Don't-care
SOP	1s	Can be treated as 1
POS	0s	Can be treated as 0

**Important Rules for Don't-Care Conditions**
*Rule 1
Don't-care cells do not have to be used.
*Rule 2
Use a don't-care only if it helps make a larger group or simplifies the expression.
*Rule 3
Don't-care cells can be used along with required 1s in SOP minimization.
*Rule 4
Don't-care cells can be used along with required 0s in POS minimization.
*Rule 5
Do not create unnecessary groups using don't-care cells.
*Rule 6
The final expression must correctly represent all required output conditions.

**ADVANTAGES**

*Simpler Boolean expressions
*Larger K-Map groups
*Fewer logic gates
*Fewer gate inputs
Reduced circuit complexity

