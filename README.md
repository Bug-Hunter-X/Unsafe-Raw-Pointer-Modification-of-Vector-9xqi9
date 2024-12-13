# Unsafe Raw Pointer Modification of Vector in Rust

This repository demonstrates a common error when using unsafe raw pointers in Rust to modify vectors.  Modifying a vector's internal data directly via a raw pointer without properly managing the vector's length can lead to undefined behavior. The example showcases this issue and demonstrates a safer, alternative approach.

## Bug

The `bug.rs` file contains code that modifies a vector using a raw pointer. This approach is unsafe because it bypasses Rust's memory safety mechanisms. While the modification works, it is not correct as it fails to update vector's length, leading to a potential data inconsistency.

## Solution

The `bugSolution.rs` file presents a safer solution that demonstrates proper vector manipulation without the use of unsafe code. It leverages Rust's built-in functionality to ensure memory safety and data integrity.