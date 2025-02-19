# Computational_Theory
# Overview

This project consists of multiple computational tasks in Python, ranging from bitwise operations to number theory and cryptographic computations. Each task is implemented with an explanation of the methodology used.

# Tasks

## Task 1: Binary Representations

    Implemented functions for bitwise operations on 32-bit unsigned integers:

    rotl(x, n): Rotates the bits of x left by n positions.

    rotr(x, n): Rotates the bits of x right by n positions.

    ch(x, y, z): Chooses bits from y where x is 1 and from z where x is 0.

    maj(x, y, z): Performs a majority vote on each bit position among x, y, and z.

## Task 2: Hash Functions

    Implemented a hash function inspired by Kernighan & Ritchie’s C hash function:

    The function iterates over the input string, updating the hash using 31 * hashval + ord(char), with a modulo 101 operation.

    The choice of 31 and 101 ensures better hash distribution and reduces collisions.

## Task 3: SHA256 Padding

    Implemented a function to compute SHA256 padding for a given file:

    Appends a 1-bit (0x80 in hex) followed by enough 0-bits to align with 512-bit blocks.

    Appends the original message length as a 64-bit big-endian integer.

    Outputs the padding in hex format.

## Task 4: Prime Numbers

    Computed the first 1,000 prime numbers using two algorithms:

    Sieve of Eratosthenes: Efficiently marks non-prime numbers and has a time complexity of O(n log log n).

    Trial Division: Checks divisibility against previously found primes, with a higher time complexity of O(n√n).