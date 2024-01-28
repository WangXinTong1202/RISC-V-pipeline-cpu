# Pipelined-CPU
A 5-stage pipeline CPU based on RISC-V instruction datasets

Table of Contents
=================

* [Directory Structure](#directory-structure)
* [CPU Design](#cpu-design)

# Directory Structure
<pre>
├── CPU(pl_computer.v)
│   ├── pl_reg_pc.v
│   ├── pl_stage_if.v  
│   │   ├── pc4.v
│   │   ├── mux4x32.v
│   │   ├── pl_instmem.v
│   ├── pl_reg_ir.v
│   ├── pl_stage_id.v
│   │   ├── regfile.v
│   │   ├── branch_addr.v
│   │   ├── jal_addr.v
│   │   ├── jalr_addr.v
│   │   ├── equ.v
│   │   ├── imme.v  
│   │   ├── mux2x32.v
│   │   ├── mux4x32.v
│   │   ├── pl_cu.v
│   ├── pl_reg_de.v
│   ├── pl_stage_exe.v
│   │   ├── alu.v
│   │   ├── mux2x32.v
│   ├── pl_reg_em.v
│   ├── pl_stage_mem.v
│   │   ├── pl_datamem.v
│   ├── pl_reg_mw.v
│   ├── pl_stage_wb.v  
│   │   ├── mux2x32.v
</pre>

# CPU Design
![](Diagrams/pipeline.png)
- 32-bit computing  
- The CPU utilizes the Harvard architecture
- Design is based on the RISC-V instruction set architecture (ISA)
- The CPU is a pipelined, single-core CPU that can execute the instructions in the base RV32I subset of the RISC-V ISA (except for those related to exceptions and interrupts).
