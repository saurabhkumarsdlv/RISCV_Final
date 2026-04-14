# RISCV_Final
College Project Final Semester
# 32-Bit RISC-V Processor with Pipelining and Hazard Management

## Overview

This project presents the design and implementation of a 32-bit RISC-V processor based on the RV32I instruction set architecture. The processor employs a five-stage pipelined architecture to improve instruction throughput and overall performance. Special emphasis is placed on hazard management techniques to ensure correct and efficient execution in a pipelined environment.

The design is developed using Verilog HDL and verified through simulation and synthesis on FPGA using Xilinx Vivado.

---

## Key Features

- 32-bit RISC-V processor supporting RV32I instruction set  
- Five-stage pipelined architecture:
  - Instruction Fetch (IF)
  - Instruction Decode (ID)
  - Execute (EX)
  - Memory Access (MEM)
  - Write Back (WB)
- Implementation of hazard management techniques:
  - Structural hazard avoidance using Harvard architecture  
  - Data hazard handling through NOP insertion  
  - Control hazard mitigation using branch control signals  
- Dual non-overlapping clock strategy for improved timing stability  
- FPGA-based simulation and synthesis using Vivado  
- Near CPI ≈ 1 performance under ideal conditions  

---

## Processor Architecture

The processor is organized into modular components to support scalability and clarity of design. The main components include:

- Instruction Memory  
- Register File  
- Arithmetic Logic Unit (ALU)  
- Control Unit  
- Data Memory  
- Pipeline Registers between each stage  

This modular structure enables efficient instruction flow and simplifies debugging and future enhancements.

---

## Pipeline Operation

Each instruction progresses through the following stages:

| Stage | Description |
|------|------------|
| IF   | Fetches instruction from instruction memory |
| ID   | Decodes instruction and reads register operands |
| EX   | Executes ALU operations |
| MEM  | Performs data memory access |
| WB   | Writes results back to the register file |

Pipelining allows multiple instructions to be processed simultaneously, thereby increasing throughput.

---

## Hazard Management

### Structural Hazards
Structural hazards are eliminated through the use of a Harvard architecture, which separates instruction and data memory paths.

### Data Hazards
Data hazards are handled using compiler-assisted NOP insertion to ensure correct operand availability during execution.

### Control Hazards
Control hazards arising from branch instructions are mitigated using a branch signal mechanism to control instruction flow.

---

## Clocking Strategy

A dual non-overlapping clock scheme is implemented to improve timing reliability and prevent metastability. This approach enhances stability during FPGA deployment and ensures proper synchronization across pipeline stages.

---

## Tools and Technologies

- Verilog HDL  
- Xilinx Vivado 2022.2  
- FPGA (for synthesis and validation)  

---

## Simulation and Results

The design was verified using RTL simulation in Vivado. The processor successfully executed a range of instruction types, including:

- Arithmetic operations  
- Logical operations  
- Memory access instructions  
- Control flow instructions  

The implementation demonstrated correct functional behavior, stable timing performance, and efficient resource utilization.

---

## Performance

- Near CPI ≈ 1 under ideal pipeline conditions  
- Improved instruction throughput due to pipelining  
- Stable execution with minimal hazards  

---

## Future Scope

Potential improvements to the current design include:

- Implementation of data forwarding techniques  
- Integration of branch prediction mechanisms  
- Addition of cache memory  
- Support for floating-point operations (FPU)  
- Extension to superscalar architecture  

---

## Project Structure
├── src/ # Verilog source files
├── testbench/ # Simulation testbenches
├── constraints/ # FPGA constraint files
├── results/ # Simulation outputs and waveforms
├── docs/ # Project documentation and report


---

## Author

Saurabh Kumar  
Bachelor of Technology (Electronics and Communication Engineering)  
Motilal Nehru National Institute of Technology Allahabad  

---

## License

This project is intended for academic and educational purposes.
