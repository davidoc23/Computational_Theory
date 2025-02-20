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

## Task 5: Roots

    Computed the first 32 bits of the fractional part of the square roots of the first 100 prime numbers. This was achieved by calculating the square root of each prime, extracting the fractional part, and converting it into a 32-bit binary representation. The approach ensures a precise representation of the mathematical property, useful in cryptographic and numerical applications.

## Task 6: Proof of Work

    Identified English words whose SHA256 hash has the highest number of leading zero bits. The word "monkey" was found to have 12 leading zero bits in its SHA256 hash digest:

    Word: monkey

    Leading Zero Bits: 12

    SHA256 Hash: 000c285457fc971f862a79b786476c78812c8897063c6fa9c045f579a3b2d63f

    To ensure that all words processed were valid English words, the NLTK words corpus was used for validation. Each word was checked against a standard dictionary before computing its SHA256 hash.