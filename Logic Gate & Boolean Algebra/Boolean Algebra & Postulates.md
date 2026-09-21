**BOOLEAN ALGEBRA**

Boolean Algebra is used to analyze and simplify the digital circuits.
Boolean Algebra allows only two possible values "0" and "1" for any variable depending upon the positive and negative logic.

**Logical OR Operation Properties**
1) A + A =A
2) A + 0 =A
3) A + 1 =A
4) A + A'=A

**Logical AND Operation Properties**
1) A . A =A
2) A . 0 =0
3) A . 1 =A
4) A . A'=0

**Boolean Laws**

NULL LAW-
A . 0 =0
A + 1 =1

IDENTITY LAW-
A . 1 =A
A + 0 =A

IDEMPOTENT LAW- 
A . A =A
A + A =A

COMPLEMENT LAW- 
A . A' =0
A + A' =1

DOUBLE NEGATION LAW- 
(A')'= A

COMMUTATIVE LAW-
A . B = B . A
A + B = B + A 

ASSOCIATIVE LAW- 
(A+B)+C = A+(B+C)
(A.B).C = A.(B.C)

DISTRIBUTIVE LAW- 
A.(B+C) = (A.B) + (A.C) 
A+(B.C) = A+B . A+C 

ABSORPTION LAW- 
A + (AB) = A
A . (A+B) =A

DE-MORGAN'S LAW-
(A+B)' = A' · B' 
(A·B)' = A' + B'

**CONSENSUS THOEREM / REDUNDANCY THEOREM**
The consensus theorem is:
AB + A'C + BC = AB + A'C
The term: BC is called the consensus term and is redundant in this expression.
This theorem can be useful for simplifying logic circuits.

Following three conditions are there for applying consensus theorem:   
There must be 3 Variables in the expression.   
1) Each variable must be repeated twice.   
2) One variable must be in the complemented form.   
3) Once above conditions are satisfied in any Boolean expression, we can only take those terms which contains the complemented variable.

**EXAMPLE OF CONSENSUS THEOREM**
Example 1: Y = AB+A'C+BC (Apply Consensus Theorem to minimize the Expression)  
Solution : Here, we have three variables A, B and C and all are repeated twice. 
The variable A is present in complemented form. 
So, all the conditions are satisfied for applying consensus theorem.   
Y = AB + A'C + BC {Redundant Term} 
After applying Redundancy theorem we can write only the terms containing complemented variables (i.e, A) and omit the Redundancy term i.e., BC. 
Hence final reduced expression would be Y = AB + A'C 

**PRINCIPLE OF DUALITY**

The principle of duality states that a valid Boolean expression remains valid when:
+ ↔ ·
0 ↔ 1
are interchanged.

Example
Original:
A + 0 = A
Dual:
A · 1 = A
Both are valid Boolean identities.



