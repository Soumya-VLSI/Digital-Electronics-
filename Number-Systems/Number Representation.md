Complements and Subtraction Using Complements

1. Introduction

Complements are an important concept in digital electronics and computer systems.

They are mainly used to:

* Represent negative numbers
* Perform subtraction using addition
* Simplify arithmetic circuits
* Reduce the need for separate subtraction hardware

There are two major types of complements:

For Binary Numbers

1. 1's Complement
2. 2's Complement

For Decimal Numbers

1. 9's Complement
2. 10's Complement

2. 1's Complement

The "1's complement" of a binary number is obtained by changing every `0` to `1` and every `1` to `0`.

Example

Find the 1's complement of:

10110110

Invert every bit:

10110110
↓
01001001

Therefore:

1's complement = 01001001

Rule

0 → 1
1 → 0

3. 2's Complement

The "2's complement" of a binary number is obtained by:

1. Finding the 1's complement
2. Adding `1`

Example

Find the 2's complement of:

10110110

Step 1: Find 1's complement

10110110
↓
01001001

Step 2: Add 1

01001001
+       1
---------
01001010

Therefore:

2's complement = 01001010

Shortcut for 2's Complement

Starting from the "rightmost bit":

* Copy bits until the first `1` is encountered.
* Keep that `1`.
* Complement all bits to its left.

Example:

10110100
       ↑
Starting from the right:

10110100
      ↑

Copy the rightmost `0`, then copy the first `1`, and complement everything to the left:

10110100
↓
01001100

Therefore:

2's complement = 01001100

4. 9's Complement

The **9's complement** is used with decimal numbers.

It is obtained by subtracting every digit from `9`.

Example

Find the 9's complement of:

5273

Perform:

9 - 5 = 4
9 - 2 = 7
9 - 7 = 2
9 - 3 = 6

Therefore:

9's complement = 4726

Shortcut

Subtract each digit from 9:

5273
↓
4726

5. 10's Complement

The "10's complement" of a decimal number is obtained by:

10's complement = 9's complement + 1

Example

Find the 10's complement of:

5273

Step 1: Find 9's complement

5273 → 4726

Step 2: Add 1

4726
+   1
-----
4727

Therefore:

10's complement = 4727

6. Subtraction Using 1's Complement

Binary subtraction can be performed using 1's complement.

Consider:

A - B

The steps are:

1. Find the 1's complement of B.
2. Add it to A.
3. Check the carry.

Case 1: End-Around Carry Exists

If a carry is generated, add that carry back to the LSB.

This is called "end-around carry".

Example

Calculate:

1011 - 0101

Step 1: Find 1's complement of 0101

0101
↓
1010

Step 2: Add to 1011

  1011
+ 1010
-------
 10101

There is an extra carry `1`.

Step 3: Add the carry to the result

0101
+  1
-----
0110

Therefore:

1011 - 0101 = 0110

Decimal verification:

11 - 5 = 6

So:

0110₂ = 6₁₀

7. Subtraction Using 2's Complement

2's complement is commonly used for binary subtraction.

To calculate:

A - B

follow these steps:

1. Find the 2's complement of B.
2. Add it to A.
3. Check the carry.

Case 1: Carry is Generated

If a carry is generated, discard the carry.

Example

1011 - 0101

Step 1: Find 2's complement of 0101

1's complement:

0101 → 1010

Add 1:

1010
+  1
-----
1011

Therefore:

2's complement of 0101 = 1011

Step 2: Add to A

  1011
+ 1011
-------
 10110

There is an extra carry `1`.

Discard the carry:

0110

Therefore:

1011 - 0101 = 0110

Decimal verification:

11 - 5 = 6

8. Subtraction Using 2's Complement When No Carry is Generated

If no carry is generated, the result is negative.

The result obtained is in "2's complement form".

To find its magnitude:

1. Take the 2's complement of the result.
2. Add a negative sign.

Example

0101 - 1011

In decimal:

5 - 11 = -6

Step 1: Find 2's complement of 1011

1's complement:

1011 → 0100

Add 1:

0100
+  1
-----
0101

Step 2: Add to 0101

  0101
+ 0101
-------
 1010

There is "no carry".

Therefore, `1010` is the 2's complement representation of the negative result.

To find the magnitude, take its 2's complement:

1010 → 0101 → +1 → 0110

Magnitude = `6`

Therefore:

0101 - 1011 = -0110

or:

= -6

9. Subtraction Using 9's Complement

Decimal subtraction can also be performed using 9's complement.

Consider:

725 - 346

Step 1: Find 9's complement of 346

346
↓
653

Step 2: Add to 725

  725
+ 653
-----
 1378

There is an end-around carry `1`.

Step 3: Add the carry to the remaining result

378
+ 1
----
379

Therefore:

725 - 346 = 379

10. Subtraction Using 10's Complement

Consider:

725 - 346

Step 1: Find 10's complement of 346

9's complement:

346 → 653

Add 1:

653 + 1 = 654

Therefore:

10's complement of 346 = 654

Step 2: Add to 725

  725
+ 654
-----
 1379

There is an extra carry `1`.

Step 3: Discard the carry

379

Therefore:

725 - 346 = 379

11. Difference Between 1's and 2's Complement

| Feature              | 1's Complement   | 2's Complement     |
| -------------------- | ---------------- | ------------------ |
| Operation            | Invert every bit | 1's complement + 1 |
| Example for `1010`   | `0101`           | `0110`             |
| Used for subtraction | Yes              | Yes                |
| End-around carry     | Required         | Not required       |
| Zero representations | Two              | One                |
| Common in computers  | Less common      | Widely used        |

12. Difference Between 9's and 10's Complement

| Feature        | 9's Complement             | 10's Complement     |
| -------------- | -------------------------- | ------------------- |
| Number system  | Decimal                    | Decimal             |
| Method         | Subtract each digit from 9 | 9's complement + 1  |
| Example: 5273  | 4726                       | 4727                |
| Carry handling | End-around carry           | Discard final carry |

13. Important Rules for Exams

1's Complement

Change 0 → 1
Change 1 → 0

2's Complement

1's complement + 1

9's Complement

Subtract every digit from 9

10's Complement

9's complement + 1

Binary subtraction using 1's complement

1. Find 1's complement of subtrahend
2. Add it to minuend
3. If carry occurs → add carry to LSB
4. If no carry → result is negative

Binary subtraction using 2's complement

1. Find 2's complement of subtrahend
2. Add it to minuend
3. If carry occurs → discard carry
4. If no carry → result is negative and is in 2's complement form

