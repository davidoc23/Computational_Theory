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

## Task 8: Bubble Sort Comparisons

This project implements Bubble Sort and tracks the number of comparisons made during the sorting process for all possible permutations of a given list of integers. The goal is to analyze how different input orders affect Bubble Sort’s efficiency in terms of comparisons.

1. **Overview**
    
    This project implements Bubble Sort and tracks the number of comparisons made during the sorting process for all possible permutations of a given list of integers. The objective is to analyze how different input orders affect Bubble Sort's efficiency in terms of comparisons.

    By applying Bubble Sort to every possible permutation of a list (e.g., [1, 2, 3, 4, 5]), we can evaluate:

    - Best-case scenario (already sorted list).
    - Worst-case scenario (completely reversed list).
    - Average-case performance for randomly ordered inputs.
    - The results are displayed in a structured table format using Python's built-in print() function.

2. **Bubble Sort Algorithm**

    Bubble Sort is a simple comparison-based sorting algorithm that works as follows:

    - Traverse the list multiple times.
    - Compare adjacent elements:
        - If they are in the wrong order, swap them.
    - Count the number of comparisons made.
        - If no swaps occur in a pass, the list is already sorted, and the algorithm terminates early (optimization).
    - Bubble Sort is generally inefficient for large lists due to its O(n²) time complexity, but this project uses it to analyze sorting behavior across different input permutations.

3. **Methodology**
    
        Step 1: Generate All Permutations

        A predefined list (e.g., [1, 2, 3, 4, 5]) is used.
        All possible permutations of the list are generated using Python’s built-in itertools.permutations.
        This ensures that all possible input orderings are tested.
        
        Step 2: Apply Bubble Sort with Comparison Counting
        
        A modified version of Bubble Sort is used.
        The algorithm counts how many times elements are compared before sorting is complete.
        The sorting process is optimized with an early exit condition (if no swaps occur, sorting stops early).
        
        Step 3: Store and Display Results
        
        Each permutation and its corresponding comparison count are stored in a list.
        The results are printed in a structured table format using Python's built-in functions.

4. **Example Output**

    When running the script, the output displays the number of comparisons needed for each permutation of [1, 2, 3, 4, 5].

        Permutation               Comparisons
        ========================================
        (1, 2, 3, 4, 5)           10
        (1, 2, 3, 5, 4)           11
        (5, 4, 3, 2, 1)           20
        (3, 1, 4, 5, 2)           14
        ...

    - Best-case scenario (sorted list) has the fewest comparisons (e.g., 10).

    - Worst-case scenario (reversed list) has the most comparisons (e.g., 20).

    - Other permutations fall between these two extremes.
