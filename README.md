# VHDL Bug: Incorrect Signal Initialization

This repository demonstrates a common bug in VHDL code: incorrect initialization of internal signals.  The bug is demonstrated in `bug.vhdl` and a corrected version is shown in `bugSolution.vhdl`.

## Bug Description

The initial value of the `internal_data` signal is not properly defined, leading to unpredictable output on the first clock cycle.  This is because uninitialized signals in VHDL can assume any value. The default value is undefined and may vary depending on the simulator.

## Solution

The solution, presented in `bugSolution.vhdl`, initializes `internal_data` to a known value (`x"00"`) to ensure predictable behavior.

This example highlights the importance of properly initializing all signals in VHDL to avoid unexpected behavior and potential design flaws. 
