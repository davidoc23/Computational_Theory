# Computational_Theory
    Project Overview

    This project implements various computational tasks related to bitwise operations, hashing, number theory, and computational complexity. The primary focus is on understanding binary representations, hash functions, prime number generation, Turing Machines, and sorting algorithms.

# Features

## 1. Binary Operations

    Bitwise Rotation:

    rotl(x, n=1): Rotates a 32-bit unsigned integer x to the left by n places.

    rotr(x, n=1): Rotates a 32-bit unsigned integer x to the right by n places.

    Bitwise Logical Operations:

    ch(x, y, z): Chooses bits from y where x has bits set to 1, and from z where x has bits set to 0.

    maj(x, y, z): Returns 1 at each bit position where at least two of x, y, and z have a 1.

## 2. Hash Functions

    A Python implementation of a hash function inspired by the one from The C Programming Language by Kernighan & Ritchie.

    Explains why prime numbers (31, 101) are used to reduce hash collisions.

    Demonstrates hashing for different input strings.

## 3. SHA256 Padding Calculation

    Implements padding for SHA256 hashing, ensuring messages conform to the 512-bit block requirement.

    Outputs the correct padding in hexadecimal format.

## 4. Prime Number Generation

    Computes the first 1,000 prime numbers using two different algorithms:

    Sieve of Eratosthenes (optimized for efficiency)

    Trial Division (optimized for correctness)

    Compares execution times of both methods.

## 5. Fractional Parts of Square Roots

    Computes the first 32 bits of the fractional part of the square roots of the first 100 prime numbers.

    Displays the results in a tabular format.

## 6. Proof of Work (SHA256 Hashing of English Words)

    Finds English words with the most leading zero bits in their SHA256 hash.

    Provides proof that the words exist in the English dictionary using NLTK.

## Task 7 - Turing Machine
Implemented a Turing Machine that adds 1 to a binary number written on its tape.

The machine starts at the left-most non-blank symbol and treats the right-most symbol as the least significant bit.

   ### Methodology:
    - The machine moves to the right-most digit of the binary number.
    - It performs addition by flipping "0" to "1" or propagating a carry by changing "1" to "0".
    - If all bits are "1", a new "1" is inserted at the start.

   ### Transition Table:

    | Current State | Read Symbol | Write Symbol | Move | Next State |
    |--------------|------------|--------------|------|------------|
    | "q0"        | "0" or "1"  | "0" or "1"   | "R"  | "q0"       |
    | "q0"        | "□"         | "□"          | "L"  | "q1"       |
    | "q1"        | "0"         | "1"          | "S"  | "qhalt"    |
    | "q1"        | "1"         | "0"          | "L"  | "q1"       |
    | "q1"        | "□"         | "1"          | "S"  | "qhalt"    |

   ### Example Execution:
   **Input Tape:** "100111"

   **Output Tape:** "101000"

    The machine processes each bit sequentially, following the transition rules above until the computation is complete.