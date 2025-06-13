# Synchronous FIFO Design and UVM-Based Verification

This project implements a synchronous FIFO (First-In-First-Out) buffer in SystemVerilog and verifies its functionality using a modular UVM (Universal Verification Methodology) testbench.

---

## 🔧 RTL Design Features

- **FIFO Type**: Synchronous (single clock domain)
- **Parameters**:
  - Configurable `DATA_WIDTH` (default: 8 bits)
  - Configurable `DEPTH` (default: 16 entries)
- **Functional Features**:
  - Write and Read operations with full/empty flag handling
  - Overflow and underflow protection
  - Blocking and non-blocking operation modes

---

## 🧪 UVM Verification Features

- **UVM Components Implemented**:
  - `fifo_transaction` – for push/pop operations
  - `fifo_sequence` – randomized transactions
  - `fifo_driver` – drives interface signals to DUT
  - `fifo_monitor` – captures and publishes observed transactions
  - `fifo_scoreboard` – checks read data against expected queue
  - `fifo_env` and `fifo_test` – top-level configuration and stimulus

- **Assertions**:
  - No write when full
  - No read when empty

- **Coverage**:
  - Functional coverage of push/pop scenarios
  - FIFO depth utilization tracking

---

## ✅ Future Scope

- Integrate protocol-level assertions (SVA)
- Extend with constrained-random and corner-case sequences
- Add coverage collection and closure metrics

---

## 🛠 Tools Used

- **Language**: SystemVerilog
- **Methodology**: UVM (IEEE 1800.2)
- **Simulation**: ModelSim / QuestaSim / EDA Playground

---

## 📌 Status

✅ In progress — testbench under development, RTL complete.  
🚀 Planned completion by [July, 2025].

---

