# FPGA Based DMA Controller Using Verilog

## Overview
This project implements a **Direct Memory Access (DMA) Controller** using **Verilog HDL**.  
The DMA controller performs autonomous memory transfers between source and destination addresses without CPU intervention.

The design is targeted for **Artix-7 FPGA devices** and developed using **Xilinx Vivado Design Suite**.  
A **Block RAM (BRAM) interface** is used to demonstrate memory read and write operations controlled by a Finite State Machine (FSM).

---

## Key Features

- RTL implementation of a **DMA Controller**
- **FSM-based control logic**
- Autonomous **memory read/write transfer**
- **BRAM interface integration**
- Parameterized **source and destination address generation**
- Modular and synthesizable Verilog design
- Designed for **FPGA-based memory systems**

---

## System Architecture

The DMA controller operates using the following states:

```
IDLE → READ → WRITE → DONE
```

### Operation Flow

1. System waits in **IDLE** state.
2. When the **start** signal is asserted, the controller enters **READ** state.
3. Data is fetched from the **source memory address**.
4. Data is written to the **destination memory address**.
5. Address pointers increment automatically.
6. After completing the transfer block, the controller enters **DONE** state.

---

## Project Structure

```
fpga-dma-controller
│
├── rtl
│   ├── dma_controller.v
│   ├── bram_interface.v
│   └── top.v
│
├── constraints
│   └── dma_constraints.xdc
│
├── sim
│   └── dma_tb.v
│
├── docs
│   └── architecture_diagram.png
│
└── README.md
```

---

## Module Description

### `dma_controller.v`
Implements the **Finite State Machine (FSM)** that controls DMA data transfer, address generation, and completion signaling.

### `bram_interface.v`
Handles memory read and write operations with **Block RAM (BRAM)**.

### `top.v`
Top-level integration module connecting the DMA controller, memory interface, and FPGA I/O.

### `dma_tb.v`
Testbench used to simulate and verify DMA controller functionality.

---

## Tools and Technologies

| Category | Tool |
|--------|--------|
| HDL | Verilog |
| FPGA | Artix-7 |
| Development Tool | Xilinx Vivado |
| Simulation | Vivado Simulator / ModelSim |
| Version Control | Git |

---

## Applications

- FPGA-based embedded systems
- High-speed memory data transfer
- Hardware accelerators
- Data buffering systems

---

## Learning Outcomes

This project demonstrates:

- RTL design using **Verilog HDL**
- **Finite State Machine (FSM)** implementation
- **FPGA memory interfacing (BRAM)**
- Hardware synthesis and implementation using **Vivado**
- Modular digital design practices

---

## License

This project is intended for **educational and research purposes**.
