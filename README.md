# Computational_Theory
## Project Overview

- This project implements various computational tasks related to bitwise operations, hashing, number theory, and computational complexity. The primary focus is on understanding binary representations, hash functions, prime number generation, Turing Machines, and sorting algorithms.

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

## 7. Turing Machine Simulation

    Implements a Turing Machine that adds 1 to a binary number.

    Simulates the binary increment operation by propagating carries.

## 8. Computational Complexity (Bubble Sort Permutations)

    Implements a Bubble Sort algorithm that counts the number of comparisons.

    Runs the sorting algorithm on all permutations of [1,2,3,4,5].

    Analyzes the complexity and outputs the comparisons for each permutation.

## Why This Project is Useful

- Educational Value: Demonstrates key computer science concepts, including bitwise operations, hashing, number theory, and algorithmic complexity.

- Cryptographic Relevance: Provides insights into SHA256 padding and bitwise operations used in cryptographic applications.

- Sorting Complexity Analysis: Highlights the performance impact of different sorting algorithms on different input permutations.

# Getting Started

## Prerequisites

    Ensure you have Python 3 installed. You may also need to install the following dependencies:

        pip install nltk

## Running the Project

Each task is implemented as a Python function and can be executed separately.

- Clone the repository:

        git clone https://github.com/davidoc23/Computational_Theory.git
    
        cd Computational_Theory


## Getting Help

    For any issues, feel free to open an issue on the GitHub repository or contact the project maintainer.

## Maintainers

    This project is maintained by David O Connor. Contributions are welcome!
