# Multicycle RISC-V Processor Core

A SystemVerilog implementation of a multicycle RISC-V processor model. This project features a custom datapath and finite state machine (FSM) control logic designed to execute a subset of RISC-V instructions, including an extended custom `ADDI` instruction implementation.

## Additional Contributors
*   https://github.com/InfyfnI

---

## Project Structure
*   `rv_top.sv`: The top-level hardware module connecting the processor components.
*   `rv_dp.sv`: The datapath module managing the register file, ALU, multiplexers, and memory interfaces.
*   `rv_ctl.sv`: The control logic module and FSM managing instruction execution states.
*   `rv_sim.sv`: The simulation testbench handling clock generation, memory loading, and timeout monitoring.
*   `params.inc`: Design parameters, instruction opcodes, and ALU control definitions.
*   `test.s`: Assembly test program used to verify standard execution and custom instruction logic.
*   `imem.hex` / `dmem_init.hex`: Hexadecimal initialization files for instruction and data memories.
*   `Dry.pdf`: Architectural documentation detailing FSM state diagrams and datapath modifications.

---

## Architectural Highlights
*   **Custom Instruction Support:** The control logic FSM includes dedicated states (`ADDI_CALC` and `ADDI_XOR`) to execute custom register-immediate calculations and bitwise operations.
*   **Datapath Expansion:** Extended routing accommodates modified multiplexer configurations for ALU input selection and constant manipulation.