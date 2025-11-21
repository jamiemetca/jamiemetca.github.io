[Back](./)

24/09/2025

# Negative numbers (The 2s complement system)

## 2s complement
2s complement is used for subtraction in binary.
0110 - 0011 (6 - 3)
Step 1 bit flip the subtractor
This is 1s complement
1100
Then add 1, 2s complement.
1101
Lastly add them
0110
1101+
----
10011
This is 4 bit math so ignore the carry and it becomes.
0011 (or 3)

## Range
Signed by numbers are said to have a range of from -(2<sup>n-1</sup> - 1) to 2<sup>n-1</sup> - 1
where n is the total number of bits
so in our example.
-(2<sup>4-1</sup>-1) = -(2^4-1) = -8
2<sup>4-1</sup> - 1  = 2^4-1 -1 =  7

## Signed numbers
When a data type says it's signed, what that means is the most significant bit (msb or rightmost bit) is used to denote the numbers negative state. 1 is negative, 0 is positive.
The negative number is also 2s complement of the positive number.
e.g. for 4 bit signed numbers
1001 is -7
0111 is 7

## Below demonstates why declaring the maximum negative interger literal causes an overflow
To demonstrate why `-8` is not a valid literal and why subtracting 1 is a safer approach, let's use a **4-bit signed integer** as an example.

---

## 1. The Literal `-8`

In a 4-bit signed integer system using two's complement, the range is from $$-2^3$$to$$2^3 - 1$$, which is **-8 to 7**.

The decimal value **8** in binary is `1000`. When the compiler sees the literal `-8`, it attempts to do the following:

1.  It creates the positive value **8** in binary: `1000`.
2.  It applies the unary negation operator (`-`). This involves flipping all the bits and adding 1.
    * Flipping `1000` gives `0111`.
    * Adding 1 gives `1000`.

This results in the bit pattern `1000`. But here's the problem: in a signed 4-bit system, `1000` is the bit pattern for **-8**. The compiler effectively has to perform a negation on a value that is already at the limit of the system, which can be problematic and lead to **undefined behavior** or a compiler warning, as the compiler has no "positive 8" to start with.

## 2. The Two-Step Process: `-7 - 1`

Now let's see how `-7 - 1` works safely.

1.  First, the compiler handles the literal **7**, which is a valid value in the 4-bit range.
    * The binary representation of 7 is `0111`.
    * The expression then becomes `-0111`. The compiler performs two's complement negation on `0111`:
        * Flip the bits of `0111`: `1000`
        * Add 1: `1001`.
    * This gives us the binary representation of **-7**, which is `1001`.

2.  Next, the compiler subtracts 1 from this result.
    * The binary representation of -7 is `1001`.
    * Subtracting 1 from `1001` gives us `1000`.

The final result, `1000`, is the correct and valid two's complement representation for **-8**, achieved without encountering any overflow or undefined behavior during the process. This two-step method is safer and more portable across different compilers.
