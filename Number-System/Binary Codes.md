BINARY CODES 

Binary codes are methods of representing numbers, letters, symbols, and other information using combinations of '0' and '1`.

Binary codes are mainly classified into:

1. Weighted Codes
2. Non-Weighted Codes
3. Alphanumeric Codes
4. Error Detection and Correction Codes

1. Weighted Codes

In a **weighted code**, each bit position has a fixed weight.

The value of the number is obtained by adding the weights corresponding to the bits that are `1`.

Common Weighted Codes

* 8421 BCD
* 2421 Code
* 5211 Code
* 84-2-1 Code

It follows the Principle Rule 

2421 is the Self Complementing Code- If sum of all the weights is 9 then it is Self Complementing Rule. 

It is Significant 

1.1 8421 BCD Code

BCD stands for **Binary Coded Decimal**.

It is a weighted code with weights:

8 4 2 1

Each decimal digit is represented separately using 4 bits.

BCD Table

| Decimal | 8421 BCD |
| ------- | -------- |
|       0 |   0000   |
|       1 |   0001   |
|       2 |   0010   |
|       3 |   0011   |
|       4 |   0100   |
|       5 |   0101   |
|       6 |   0110   |
|       7 |   0111   |
|       8 |   1000   |
|       9 |   1001   |

Codes from 1010 to 1111 are invalid in 8421 BCD.

Example

Convert decimal 25 to BCD:

2 → 0010
5 → 0101

Therefore:

25 = 0010 0101 (BCD)

Note:

25 in binary = 11001
25 in BCD    = 0010 0101

2. Non-Weighted Codes

In a **non-weighted code**, the bit positions do not have fixed weights.

The value cannot be obtained simply by adding predefined bit weights.

Common Non-Weighted Codes

* Excess-3
* Gray Code

2.1 Excess-3 Code

Excess-3, also called **XS-3**, is a non-weighted decimal code.

Is a self complementing and it can obtain from BCD. 

To obtain Excess-3:

1. Add '3` to each decimal digit.
2. Convert the result to 4-bit binary.

Example

Convert '5` to Excess-3:

5 + 3 = 8

8 = 1000

Therefore:

5 = 1000 (Excess-3)

Example: 25

Convert each digit separately:

2 + 3 = 5 → 0101
5 + 3 = 8 → 1000

Therefore:

25 = 0101 1000 (Excess-3)

Excess-3 Table

| Decimal | Excess-3 |
| ------- | -------- |
|       0 |   0011   |
|       1 |   0100   |
|       2 |   0101   |
|       3 |   0110   |
|       4 |   0111   |
|       5 |   1000   |
|       6 |   1001   |
|       7 |   1010   |
|       8 |   1011   |
|       9 |   1100   |

2.2 Gray Code

Gray code is a non-weighted code in which **only one bit changes between two consecutive values**.

Used in K-Map it can obtain from bianry number only .

3-bit Gray Code

| Decimal | Binary | Gray |
| ------- | ------ | ---- |
|       0 |   000  |  000 |
|       1 |   001  |  001 |
|       2 |   010  |  011 |
|       3 |   011  |  010 |
|       4 |   100  |  110 |
|       5 |   101  |  111 |
|       6 |   110  |  101 |
|       7 |   111  |  100 |

Binary to Gray Conversion

Rules:

Gray MSB = Binary MSB

Next Gray bit = Previous Binary bit XOR Current Binary bit

Example:

Binary = 1011
G3 = 1
G2 = 1 XOR 0 = 1
G1 = 0 XOR 1 = 1
G0 = 1 XOR 1 = 0

Therefore:

1011₂ = 1110 Gray

Applications

Gray code is used in:

* Digital communication
* ADCs
* Karnaugh maps

3. Alphanumeric Codes

Alphanumeric codes represent:

* Alphabets
* Numbers
* Special characters
* Symbols

Common alphanumeric codes include:

1. ASCII
2. EBCDIC
3. Unicode

3.1 ASCII

ASCII stands for:

**American Standard Code for Information Interchange**

Standard ASCII uses **7 bits**.

Therefore, it can represent:

2^7 = 128 characters.

Common ASCII Values

| Character | Decimal ASCII |
| --------- | ------------- |
|     A     |            65 |
|     B     |            66 |
|     C     |            67 |
|     a     |            97 |
|     b     |            98 |
|     0     |            48 |
|     1     |            49 |
|   Space   |            32 |

Example:

A = 65₁₀ = 1000001₂

ASCII is widely used in computers and communication systems.

3.2 EBCDIC

EBCDIC stands for:

**Extended Binary Coded Decimal Interchange Code**

It is an **8-bit character encoding** developed by IBM.

Since it uses 8 bits:

2^8 = 256

possible code combinations are available.

It was mainly used in IBM mainframe and related computer systems.

3.3 Unicode

Unicode is a universal character encoding standard.

It supports characters from many languages as well as:

* Mathematical symbols
* Technical symbols
* Emojis
* Special characters

Unlike ASCII, Unicode is designed to support a very large number of characters.

4. ANSI Codes

ANSI stands for:

**American National Standards Institute**

ANSI is a standards organization rather than a single binary code.

ANSI has been associated with standards used in:

* Computers
* Electronics
* Communication
* Character encoding

ANSI Character Codes

In many older computing contexts, "ANSI codes" may refer to character-code conventions or escape sequences used by terminals.

For basic digital electronics studies, the more important character code to remember is **ASCII**.

5. IEEE Standards

IEEE stands for:

**Institute of Electrical and Electronics Engineers**

IEEE develops standards for electrical, electronic, computer, and communication systems.

IEEE standards are not a single type of binary code.

Important IEEE Standards

| Standard    | Application                   |
| ----------- | ----------------------------- |
| IEEE 754    | Floating-point representation |
| IEEE 802.3  | Ethernet                      |
| IEEE 802.11 | Wireless LAN / Wi-Fi          |

IEEE 754

IEEE 754 defines the representation and arithmetic of floating-point numbers.

A typical floating-point representation contains:

Sign | Exponent | Fraction

For example, a 32-bit single-precision floating-point number contains:

1 bit  → Sign
8 bits → Exponent
23 bits → Fraction

Total: 32 bits

