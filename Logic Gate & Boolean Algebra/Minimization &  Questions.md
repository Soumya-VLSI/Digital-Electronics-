**MINIMIZATION OF BOOLEAN EXPRESSION**

1. Introduction

Boolean minimization is the process of simplifying a Boolean expression into an equivalent expression with fewer terms and variables.

The minimized expression produces the same output as the original expression but requires less hardware.

Main objectives
Reduce the number of logic gates
Reduce the number of gate inputs
Reduce circuit complexity
Reduce propagation delay
Reduce power consumption
Reduce hardware area
2. Methods of Boolean Minimization

Boolean expressions can mainly be minimized using:

Boolean Algebra
Karnaugh Map (K-Map)
Quine-McCluskey Method

For basic digital circuit design, Boolean Algebra and K-Maps are commonly used.

**IMPORTANT QUESTIONS**

Ques1. A'B + AB + A'B' + BC 
Sol 1. B ( A'+ A) + A'B' + BC 
       B + (A'B') + BC 
       B + BC + A'B' 
       B ( 1 + C) + A'B' 
       B + (A'B' ) 
       B + A'

Ques2. F=0 (when input equal)
       F=1 (when input different)
       ABC + A'BC' is high for all combinations except all input equals. 

Ques3. No of Self Dual Boolean functions of 4 variable ?
Sol 3. 4 variables 
       2^4 =16 
       F(A,B,C,D)=F(A',B'C',D')'
       16 input combinations form 8 pairs.
       Formula: 2^2^(n-1) = 2^3 = 8 

Ques4. F(A,B,C) =F(A',B' ,C')'
Sol 4. This is called self dual 

Ques5. F = A ⊕ B ⊕ C ⊕ D
Sol 5. XOR for odd number of 1's =1 
       F = A ⊕ B ⊕ C ⊕ D =1 

Ques6. (A+B+C') (A+B'+C) (A'+B+C) 
Sol 6. ( 001) (101) (011) 
           (1,2,4)
         (0,3,5,6,7) 
         Therefore the number of literals in (A+B+C') (A+B'+C) (A'+B+C) is 5.


