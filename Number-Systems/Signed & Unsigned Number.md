Signed and Unsigned Number Representation

1. Introduction

In digital systems, binary numbers can be represented in two ways:

1. Unsigned representation
2. Signed representation

The main difference is whether the binary number is allowed to represent "negative values".

* Unsigned numbers represent only positive numbers and zero.
* Signed numbers represent both positive and negative numbers.

2. Unsigned Number Representation

In an unsigned binary number, "all bits are used to represent the magnitude of the number".

There is no separate sign bit.

Example: 8-bit unsigned number

10110110

Its decimal value is:

1(2^7)+0(2^6)+1(2^5)+1(2^4)+0(2^3)+1(2^2)+1(2^1)+0(2^0)

=128+32+16+4+2

=182

Therefore:

10110110₂ = 182₁₀

3. Range of Unsigned Numbers

For an "n-bit unsigned number", the range is:

0 to 2^n-1

Example: 4-bit unsigned number
0 to 2^4-1
=0 to 15

Therefore:

| Number of bits | Unsigned range |
| -------------: | -------------: |
|          1 bit |         0 to 1 |
|         2 bits |         0 to 3 |
|         3 bits |         0 to 7 |
|         4 bits |        0 to 15 |
|         8 bits |       0 to 255 |

4. Signed Number Representation

Signed binary numbers can represent both:

* Positive numbers
* Negative numbers

Usually, the **MSB (Most Significant Bit)** is used as the **sign bit**.

For a commonly used 2's-complement representation:

MSB = 0 → Positive
MSB = 1 → Negative

Example

For an 8-bit signed number:

01010101

MSB = `0`, so the number is positive.

11010101

MSB = `1`, so the number is negative in 2's-complement representation.

5. Sign Bit

The leftmost bit is called the **Most Significant Bit (MSB)**.

In signed 2's-complement representation:

0 → Positive
1 → Negative

Example:

01001010
↑
Sign bit

Since the sign bit is `0`, the number is positive.

For:

11001010
↑
Sign bit

The sign bit is `1`, so the number is negative.

6. Methods of Signed Number Representation

There are three commonly studied methods:

1. Sign-Magnitude
2. 1's Complement
3. 2's Complement


7. Sign-Magnitude Representation

In sign-magnitude representation:

* MSB represents the sign.
* Remaining bits represent the magnitude.

0 → Positive
1 → Negative

Example

Represent +5 and -5 using 8 bits.

Binary representation of 5:

0000101

For +5:

0 0000101
↑
Sign bit

+5 = 00000101

For -5:

1 0000101

-5 = 10000101

Important point

Sign-magnitude has **two representations of zero**:

00000000 → +0
10000000 → -0

8. 1's Complement Representation

In 1's-complement representation, a negative number is obtained by taking the **1's complement of its positive representation**.

Example: Represent -5 using 8 bits

First represent +5:

00000101

Take 1's complement:

11111010

Therefore:

-5 = 11111010

Again, 1's complement has two representations of zero:

00000000 → +0
11111111 → -0

9. 2's Complement Representation

2's complement is the most commonly used method for representing signed integers in modern digital systems.

To obtain the negative representation:

1. Write the positive number in binary.
2. Find its 1's complement.
3. Add 1.

Example: Represent -5 using 8 bits

Positive 5:

00000101

1's complement:

11111010

Add 1:

11111010
+      1
---------
11111011

Therefore:

-5 = 11111011

10. Range of Signed 2's-Complement Numbers

For an "n-bit signed 2's-complement number", the range is:

-2^{n-1 to 2^{n-1}-1

Example: 4-bit signed number

-2^{3} to  2^{3}-1

=-8 + 7

Therefore:

4-bit signed range = -8 to +7

8-bit signed range

-2^7 to 2^7-1
=-128 + 127

Therefore:

8-bit signed range = -128 to +127

14. Why Signed and Unsigned Representation is Important

Signed and unsigned representations are important in:

* Digital electronics
* VLSI
* Verilog/SystemVerilog
* Computer architecture
* Embedded systems

In Verilog, the distinction is especially important because arithmetic and comparisons can produce different results depending on whether signals are treated as signed or unsigned.


