WHAT IS BIT?
A bit is the smallest unit of data in a computer.
A bit can be 1 or o that is it!
computer uses binary number system for data like 0 or 1
| Decimal | Binary |
|---:|:---:|
| 0 | 0000 |
| 1 | 0001 |
| 2 | 0010 |
| 3 | 0011 |
| 4 | 0100 |
| 5 | 0101 |
| 6 | 0110 |
| 7 | 0111 |
| 8 | 1000 |
| 9 | 1001 |
| 10 | 1010 | a
| 11 | 1011 |b
| 12 | 1100 |c
| 13 | 1101 |d
| 14 | 1110 |e
| 15 | 1111 |f

SOME OF THE BITWISE OPERATORS ARE :

& , | , ^ , << , >> , ~ .
STAGE 2:
BITWISE AND(&):

DEFINITION: 
it produces 1 only when both corresponding bits are 1.otherwise it gives 0.

| A | B | A & B |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

RIGHT SHIFT: LOGICAL SHIFT Vs. ARITHEMETIC SHIFT:
int x = 8;
x = x >> 1;

Before:  00001000
                 >>
After:   00000100
The rightmost bit is removed, and a new bit enters from the left.

there are two ways to fill that new position.
A.LOGICAL RIGHT SHIFT:

IN LOGICAL RIGHT SHIFT, THE VACATED BITS ARE ALWAYS FILLED WITH 0.

Before:  10001000

After:   01000100
         ↑
         0 inserted

B.ARITHEMETIC RIGHT SHIFT:

IN ARITHEMETIC RIGHT SHIFT, THE VACANT POSITIONS ARE FILLED WITH THE SIGN BIT.

THE SIGN BIT IS THE LEFTMOST BIT :
0-- means nonnegative
1--means negative(in the usual signed integer representation).

Before:  10001000

After:   11000100
         ↑
         1 inserted

NOTICE THE DIFFERENCE:

Logical:    01000100
Arithmetic: 11000100

IMPORTANT C LANGUAGE DETAIL: right-shifting a negative signed integer is implementation defined. the compiler/platform determines how it behaves. most modern systems use arithmetic right shift.

if the operand is an unsigned integer or signed nonnegative integer, the vacant positions are filled with zeros.

USING UNSIGNED INTEGER:

unsigned int x = 8;
x = x >> 1;

00001000
     >> 
00000100      4

SIGNED NONNEGATIVE INTEGER

int x = 8;
x = x >> 1;

00001000
     >>
00000100    4

WHAT ABOUT NEGATIVE INTEGERS:

int x = -8;
x = x >> 1;

THE RESULT IS IMPLEMENTATION- DEFINED IN C.






