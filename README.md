# Java Race Condition Example

This repository demonstrates a common race condition in Java multithreaded programming.  The `Counter` class attempts to increment a shared counter variable, but without proper atomicity, the final count may be less than expected when multiple threads concurrently access and modify it.

## Problem

The `increment()` method is not atomic; multiple threads can interleave their execution, leading to lost updates.

## Solution

The solution involves using the `AtomicInteger` class, providing atomic operations that guarantee thread safety.