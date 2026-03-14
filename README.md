# RPS-FSMD-Verilog-SiS

Hardware implementation of a **Finite State Machine with Datapath (FSMD)** 
for the Rock-Paper-Scissors game, developed as part of the Computer 
Architecture course at the University of Verona (2024).

## Implementation

- **RTL level**: SystemVerilog (`design.sv`) with full testbench (`testbench.sv`)
- **Gate level**: SiS synthesis from BLIF description (`SRC/sis/`)
- Both optimized and non-optimized gate-level netlists included

## Repository Structure

| File/Folder | Description |
|---|---|
| `design.sv` | FSMD RTL description in SystemVerilog |
| `testbench.sv` | Simulation testbench |
| `SRC/sis/` | Gate-level BLIF modules (SiS) |
| `SRC/*.pdf` | Project report |

## How to Run

**Verilog simulation:**
```bash
# Any standard Verilog simulator (e.g. ModelSim, Icarus)
iverilog -o rps design.sv testbench.sv && vvp rps
