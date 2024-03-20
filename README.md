# Bit Manipulation Guide

## Table of Contents

- [Decimal Number System](#decimal-number-system)
- [Octal Number System](#octal-number-system)
- [Binary Number System](#binary-number-system)
- [Storing Negative Number](#storing-negative-number)
- [Signed and Unsigned Data Types](#signed-and-unsigned-data-types)
- [Data Ranges](#data-ranges)
- [Bitwise Operators](#bitwise-operators)

---

## Decimal Number System

The decimal number system is a base-10 numbering system that uses ten digits (0-9) to represent numerical values, with each position in a number representing a power of 10.

Position:  10^3   10^2   10^1   10^0  
Value:        3      4      5      6  

Example:  
The integer 3456 is represented in the decimal number system.

## Octal Number System

The octal number system is a base-8 numbering system that uses eight digits (0-7) to represent numerical values.

Example:  
Let's represent the octal integer 347 in the octal number system:

Position:  8^2   8^1   8^0  
Value:      3     4     7  

Conversion of Octal number to decimal number:

347 (Octal)  
= (3 × 8^2) + (4 × 8^1) + (7 × 8^0)  
= (3 × 64) + (4 × 8) + (7 × 1)  
= (192) + (32) + (7)  
= 231 (Decimal)

## Binary Number System

The binary number system is a base-2 numbering system that uses two digits, 0 and 1, to represent numerical values. In binary, each digit's position signifies its weight, doubling in value with each position.

Example:  
Conversion of binary to decimal:

101011 (Binary)  
= (1 × 2^5) + (0 × 2^4) + (1 × 2^3) + (0 × 2^2) + (1 × 2^1) + (1 × 2^0)  
= 32 + 0 + 8 + 0 + 2 + 1  
= 43 (Decimal)

Conversion of decimal to binary:

43 ÷ 2 = 21 remainder 1  
21 ÷ 2 = 10 remainder 1  
10 ÷ 2 = 5 remainder 0  
5 ÷ 2 = 2 remainder 1  
2 ÷ 2 = 1 remainder 0  
1 ÷ 2 = 0 remainder 1  

43 (Decimal) = 101011 (Binary)

## Storing Negative Number

In binary representation, negative integers are typically stored using a method called two's complement.

### Two's Complement:

In two's complement, the leftmost bit (most significant bit) is used as a sign bit. If this bit is 0, the number is positive; if it's 1, the number is negative. To get the two's complement of a negative number, first, take the binary representation of its positive counterpart (absolute value), then invert all the bits, and finally add 1 to the result.

Example:  
Let's store the decimal number -5 in binary using two's complement:

1) Get the binary representation of the positive counterpart of 5:  
   5 (Decimal) = 00000101 (Binary)

2) Invert all the bits:  
   Invert: 11111010

3) Add 1 to the result:  
   Result: 11111011

So, the binary representation of -5 using two's complement is 11111011.

## Signed and Unsigned Data Types

### Signed Data Type

Signed data types represent both positive and negative numbers, using one bit to represent the sign and the remaining bits to represent the magnitude of the number.

Example:

Signed integers in Java, such as `int` or `long`, are signed data types. For example:

- `int`: Range from -2,147,483,648 to 2,147,483,647.
- `long`: Range from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.

### Unsigned Data Type

Unsigned data types represent only non-negative numbers (zero and positive numbers) using all bits to represent the magnitude of the number without a sign bit.

Example:

Unsigned integers are not directly supported in Java, but you can use larger signed integer types or manipulate the bits manually to represent unsigned integers.

### Data Ranges

| Data Type | Range                                   |
|-----------|-----------------------------------------|
| byte      | -128 to 127                             |
| short     | -32,768 to 32,767                       |
| int       | -2,147,483,648 to 2,147,483,647         |
| long      | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| float     | Approximately ±3.40282347E+38F         |
| double    | Approximately ±1.79769313486231570E+308 |
| char      | 0 to 65,535                             |
| boolean   | True or False                           |

## Bitwise Operators

| Operator   | Description      | Example                    |
|------------|------------------|----------------------------|
| `&`        | Bitwise AND      | `int result = 5 & 3; // 1` |
| `|`        | Bitwise OR       | `int result = 5 \| 3; // 7`|
| `^`        | Bitwise XOR      | `int result = 5 ^ 3; // 6` |
| `~`        | Bitwise NOT      | `int result = ~5; // -6`   |
| `<<`       | Left Shift       | `int result = 5 << 2; // 20`|
| `>>`       | Right Shift      | `int result = 20 >> 2; // 5`|
| `>>>`      | Unsigned Right Shift | `int result = -20 >>> 2; // 1073741829`|

### Left Shift (`<<`)

```java
int num = 5; // Binary: 00000000000000000000000000000101
int result = num << 2; // Binary: 00000000000000000000000000010100 (Decimal: 20) 
```
### Right Shift (`>>`)
```java
int num = 20; // Binary: 00000000000000000000000000010100
int result = num >> 2; // Binary: 000000000000000000000000000
```

### Practice Problems on Bit Manipulation

| Difficulty | Problem                                                                  |
|------------|--------------------------------------------------------------------------|
| Easy       | [Reverse Bits](https://leetcode.com/problems/reverse-bits/description/) |
| Easy       | [Power of Two](https://leetcode.com/problems/power-of-two/description/) |
| Easy       | [Missing Number](https://leetcode.com/problems/missing-number/description/) |
| Easy       | [Binary Number with Alternating Bits](https://leetcode.com/problems/binary-number-with-alternating-bits/description/) |
| Easy       | [Find the Difference](https://leetcode.com/problems/find-the-difference/description/) |
| Easy       | [Power of Four](https://leetcode.com/problems/power-of-four/description/) |
| Easy       | [Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/description/) |
| Medium     | [Single Number II](https://leetcode.com/problems/single-number-ii/description/) |
| Medium     | [Sum of Two Integers](https://leetcode.com/problems/sum-of-two-integers/description/) |



