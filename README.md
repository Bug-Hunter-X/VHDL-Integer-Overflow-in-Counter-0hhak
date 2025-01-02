# VHDL Integer Overflow Bug

This repository demonstrates a common error in VHDL: integer overflow in a counter.  The `buggy_counter.vhdl` file contains code for a simple counter that is susceptible to overflow.  The `buggy_counter_fixed.vhdl` file shows how to correct this issue using a more robust approach.

## Problem

The original code uses a standard `integer` type for the counter.  When the counter reaches its maximum value (15 in this case), incrementing it leads to undefined behavior.  Simulators might wrap around to 0, or other unexpected results could occur.

## Solution

The solution involves better handling of the counter's limit.  The corrected code prevents overflow by explicitly checking the counter's value before incrementing.  Alternative solutions might include using unsigned types or implementing a modulo operator.