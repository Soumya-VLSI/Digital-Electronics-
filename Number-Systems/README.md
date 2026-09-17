1. Introduction

A number system is a method of representing numerical values using a specific set of symbols or digits.

Number systems are fundamental to digital electronics because digital circuits operate primarily using two logic states:

Logic 0
Logic 1

Understanding number systems is essential for digital logic design, computer architecture, microprocessors, Verilog HDL, FPGA design, and VLSI.

2. Types of Number Systems

The commonly used number systems in digital electronics are:

Number System	Base (Radix)	Digits Used
Decimal	10	0–9
Binary	2	0, 1
Octal	8	0–7
Hexadecimal	16	0–9, A–F

The base (radix) indicates the number of unique digits used in the number system.

3. Decimal Number System

The decimal number system has a base of 10.

It uses the digits:

0, 1, 2, 3, 4, 5, 6, 7, 8, 9

Each position represents a power of 10.

Example

583

The expanded form is:

583 = 5 × 10² + 8 × 10¹ + 3 × 10⁰

583 = 500 + 80 + 3

Therefore:

583₁₀ = 583 

4. Binary Number System

The binary number system has a base of 2.

It uses only two digits:

0 and 1

Each binary digit is called a bit.

The position of each bit represents a power of 2.

Example

1011₂

Its decimal equivalent is:

1011₂ = 1 × 2³ + 0 × 2² + 1 × 2¹ + 1 × 2⁰

= 8 + 0 + 2 + 1

= 11₁₀

Therefore:

1011₂ = 11₁₀

5. Octal Number System

The octal number system has a base of 8.

It uses the digits:

0, 1, 2, 3, 4, 5, 6, 7

Each position represents a power of 8.

Example

157₈

157₈ = 1 × 8² + 5 × 8¹ + 7 × 8⁰

= 64 + 40 + 7

= 111₁₀

Therefore:

157₈ = 111₁₀

6. Hexadecimal Number System

The hexadecimal number system has a base of 16.

It uses:

0–9 and A–F

The letters represent:

Hexadecimal	Decimal
A	10
B	11
C	12
D	13
E	14
F	15
Example

2F₁₆

2F₁₆ = 2 × 16¹ + 15 × 16⁰

= 32 + 15

= 47₁₀

Therefore:

2F₁₆ = 47₁₀

7. Number System Conversions

Number-system conversion means changing a number from one number system to another while representing the same numerical value.

Convert Other Base System to Non-Decimal System : 
Convert original number to decimal number (base 10) and then convert the decimal number to new base number. 

Common conversions include:

Binary → Decimal
Decimal → Binary
Binary → Octal
Octal → Binary
Binary → Hexadecimal
Hexadecimal → Binary
Decimal → Octal
Decimal → Hexadecimal

8. Binary to Decimal Conversion

To convert binary to decimal, multiply each bit by its corresponding power of 2 and add the results.

Example

1101₂ → Decimal

1101₂ = 1 × 2³ + 1 × 2² + 0 × 2¹ + 1 × 2⁰

= 8 + 4 + 0 + 1

= 13₁₀

Therefore:

1101₂ = 13₁₀

9. Decimal to Binary Conversion

To convert a decimal integer to binary, repeatedly divide the number by 2 and record the remainders.

Example

Convert:

13₁₀ → Binary

13 ÷ 2 = 6 remainder 1
 6 ÷ 2 = 3 remainder 0
 3 ÷ 2 = 1 remainder 1
 1 ÷ 2 = 0 remainder 1

Read the remainders from bottom to top:

1101₂

Therefore:

13₁₀ = 1101₂

10. Binary to Octal Conversion

For binary-to-octal conversion, group the binary digits into groups of 3 bits starting from the right.

Example

101101₂ → Octal

Group into 3 bits:

101 101

Convert each group:

101₂ = 5₈
101₂ = 5₈

Therefore:

101101₂ = 55₈

11. Octal to Binary Conversion

Each octal digit can be represented using exactly 3 binary bits.

Example

57₈ → Binary

5 → 101
7 → 111

Therefore:

57₈ = 101111₂

12. Binary to Hexadecimal Conversion

For binary-to-hexadecimal conversion, group the binary digits into groups of 4 bits starting from the right.

Example

10101111₂ → Hexadecimal

Group into 4 bits:

1010 1111

Convert each group:

1010₂ = A₁₆
1111₂ = F₁₆

Therefore:

10101111₂ = AF₁₆

13. Hexadecimal to Binary Conversion

Each hexadecimal digit can be represented using exactly 4 binary bits.

Example

3A₁₆ → Binary

3 → 0011
A → 1010

Therefore:

3A₁₆ = 00111010₂
