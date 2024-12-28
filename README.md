# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL: counter overflow.  The provided VHDL code implements a simple counter, but lacks a mechanism to prevent overflow when the counter reaches its maximum value. This can lead to unexpected behavior or simulation errors.

## Bug Description
The `counter` entity increments its internal count without checking if it has reached the upper bound (7). Once the counter reaches 7, the next increment results in an overflow, leading to undefined behavior.  The behavior depends on the simulator's handling of overflow, but might result in wrapping around to 0 or causing a simulation error.

## Solution
The solution involves adding a check to prevent the counter from exceeding its maximum value.  The modified code explicitly handles the case where `internal_count` reaches 7, preventing the overflow.