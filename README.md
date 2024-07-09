# pipelined-mips32-processor
## Overview

This project implements a pipelined MIPS32 processor in Verilog. It includes the main processor module, a testbench for simulation, and the generated waveform file to analyze the results. The processor supports basic arithmetic, logical, memory, and control instructions.

## Files

- `main.v`: Contains the Verilog code for the pipelined MIPS32 processor.
- `main_tb.v`: Contains the testbench for the processor to simulate and verify its functionality.
- `main_tb.vcd`: Value Change Dump (VCD) file generated from the simulation, used to visualize the waveform.

## Processor Description

The pipelined MIPS32 processor consists of the following stages:

1. **Instruction Fetch (IF)**: Fetches the instruction from memory using the program counter (PC).
2. **Instruction Decode (ID)**: Decodes the instruction and reads the required registers.
3. **Execution (EX)**: Performs arithmetic or logical operations.
4. **Memory Access (MEM)**: Accesses memory for load and store instructions.
5. **Write Back (WB)**: Writes the result back to the register file.

The processor supports a subset of the MIPS32 instruction set, including:

- Arithmetic operations: ADD, SUB, MUL, DIV, etc.
- Logical operations: AND, OR, SLL, SRL, etc.
- Memory operations: LW, SW
- Control operations: BEQ

## Testbench Description

The testbench (`main_tb.v`) initializes the processor, loads a set of instructions into memory, and runs the simulation. The testbench also includes a clock generation block to provide the necessary clock signals for the processor.

### Simulation

To run the simulation:

1. Load the `main.v` and `main_tb.v` files into your Verilog simulation tool.
2. Compile the files.
3. Run the simulation to generate the `main_tb.vcd` file.
4. Use a waveform viewer to open the `main_tb.vcd` file and analyze the results.

## Getting Started

### Prerequisites

- Verilog simulation tool (e.g., ModelSim, Vivado)
- Waveform viewer (e.g., GTKWave)

### Running the Simulation

1. **Compile the Verilog Files**: 
   ```shell
   vlog main.v main_tb.v

