1. Number System Conversions

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

2. Binary to Decimal Conversion

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

QUES. How many minimum number of bits are required to represent 2500 in binary

ANS. To find the minimum number of bits required to represent 2500 in binary:

We need to find the smallest (n) such that:

2^n > 2500 

Check powers of 2:

2^{11}=2048 
2^{12}=4096

Since:

2048 < 2500 < 4096

we need 12 bits.

For verification:

2500_{10} = 100111000100_2 

There are 12 binary digits.

Shortcut for exams:

{Number of bits}=log_2(N)+1} 

QUES. 312/20=13.1 in which radix is this possible? 

ANS. We need to find the radix (base) in which:

(312)_r \div (20)_r = (13.1)_r 
Step 1: Convert each number into decimal form
(312)_r = 3r^2 + 1r + 2 
(20)_r = 2r 
(13.1)_r = r + 3 + 1/r

So:
{3r^2+r+2}/{2r} = r+3+1/r

Step 2: Multiply both sides by \(2r\)
3r^2+r+2=2r^2+6r+2 

Bring everything to one side:

r^2-5r=0 
r(r-5)=0 

Since radix cannot be 0:

r=5
	​
 
QUES. (2101222012.120212)3=( )9

ANS. We need to convert:

(2101222012.120212)_3 = (?)_9 

Since:

9=3^2 

we can convert base 3 → base 9 by grouping the ternary digits in pairs, starting from the radix point.

Step 1: Group the digits

For the integer part, group from right to left:

2101222012 

Add a zero on the left if needed:

21 | 01 | 22 | 01 | 2 

The last group needs two digits:

21 | 01 | 22 | 01 | 02 

For the fractional part, group from left to right:

120212 
12 | 02 | 12 

So:

(21 | 01 | 22 | 01 | 02 . 12 | 02 | 12)_3 

Step 2: Convert each pair from base 3 to base 9
Base-3 pair	Decimal value	Base-9 digit
21	2(3)+1 =	7
01  0(3)+1 =	1
22	2(3)+2 =	8
01	1       	1
02	2        	2
12	1(3)+2 =	5
02	2	        2
12	5	        5

Therefore:
{(2101222012.120212)_3=(71812.525)_9}
(71812.525)9​

	​
