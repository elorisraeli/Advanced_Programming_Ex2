# Prime Number Counter with Multithreading

## Overview

This project demonstrates an advanced implementation of a prime number counter that processes an endless stream of data using multithreading techniques.
The goal is to efficiently utilize CPU cores to achieve significant performance improvements over a provided baseline implementation.

## Problem Statement

Given a random number generator (`randomGenerator`) that simulates an endless data stream and a basic prime counter application (`primeCounter`).
Our task is to create a more efficient prime number counter that processes the stream in parallel while using no more than 2MB of RAM.

## Objectives

- Implement a multithreaded prime number counter.
- Optimize the `isPrime` function for better performance.
- Ensure RAM usage does not exceed 2MB.
- Achieve at least 4 times better performance without improving `isPrime`.
- Achieve at least 10 times better performance with an improved `isPrime`.
- Explore CPU and memory consumption of the solution in detail.

## Usage

### Prerequisites

- A Unix-like operating system (Linux, macOS).
- Make sure you have the `time` command available to measure the performance.

### Files Provided

- `randomGenerator` - Generates a stream of random numbers.
- `primeCounter` - Baseline implementation of the prime number counter.

### Running the Baseline Implementation

To generate numbers and count primes using the provided baseline:

```sh
./randomGenerator <seed> <num_of_numbers> | ./primeCounter
```

Example:    
```sh
./randomGenerator 10 10000000 | ./primeCounter
```

This will generate 10 million random numbers with a seed of 10 and pipe them to the primeCounter program.

### Running Your Solution
To run your optimized prime number counter:
```sh
./randomGenerator <seed> <num_of_numbers> | ./optimizedPrimeCounter
```

Example:

```sh
./randomGenerator 10 10000000 | ./optimizedPrimeCounter
```

This will generate 10 million random numbers with a seed of 10 and pipe them to your optimizedPrimeCounter program.

### Measuring Performance
Use the time command to measure the performance of both implementations:

```sh
time ./randomGenerator 10 10000000 | ./primeCounter
time ./randomGenerator 10 10000000 | ./optimizedPrimeCounter
```

## Submission Requirements
1. Solution Code: Provide your optimized solution code along with instructions on how to run it (makefile, scripts, etc.).

2. Baseline Performance Screenshot: Screenshot of the performance result of the provided primeCounter with 10 million numbers.

3. Optimized Performance Screenshot: Screenshot of the performance result of your optimizedPrimeCounter with 10 million numbers.

4. RAM Usage Proof: Proof that your solution uses less than 2MB of RAM.

## Performance Expectations
At least 4 times better performance without improving isPrime function (90% mark).
At least 10 times better performance with an improved isPrime function (10% mark).
Additional Information
For more information on implementing a lock-free queue, refer to the Schneems Blog.

## Disclaimer
Changing CPU to performance mode may overheat your machine. If unsure, use a PC at the campus labs. No warranties are provided for your own device.


### Contributors
Elor Israeli and Roni Michaeli
