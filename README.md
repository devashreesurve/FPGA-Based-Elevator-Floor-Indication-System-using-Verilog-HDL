# FPGA-Based-Elevator-Floor-Indication-System-using-Verilog-HDL
Finite State Machine (FSM) based Elevator Floor Indication System implemented in Verilog HDL on AMD Spartan-7 FPGA using Vivado.

## Project Overview

This project implements a Finite State Machine (FSM) based Elevator Floor Indication System using Verilog HDL on the AMD Spartan-7 FPGA Development Board.

The system simulates the movement of an elevator between two floors using push-button inputs while displaying the elevator's current position using onboard LEDs.

The primary objective of this project is to demonstrate the implementation of digital control systems on an FPGA through hardware description language (HDL) and finite state machine design.

---


# Features

 Finite State Machine (FSM) Based Design

Real-Time FPGA Implementation

Two Floor Elevator Simulation

Push Button Inputs

- UP Button
- DOWN Button
- RESET Button

LED Floor Indication
Verilog HDL Design
RTL Simulation
FPGA Synthesis
Hardware Verification
Xilinx Vivado Compatible

---

# Hardware Specifications

| Component | Description |
|------------|-------------|
| FPGA Board | AMD Spartan-7 Development Board |
| FPGA Device | XC7S50CSGA324-1 |
| Input Devices | Push Buttons |
| Output Devices | Onboard LEDs |
| Programming Tool | Vivado Hardware Manager |

---

# Software Requirements

- Xilinx Vivado Design Suite
- Verilog HDL
- Windows/Linux
- FPGA Programmer
- Simulation Tool (Vivado Simulator)




# Finite State Machine (FSM)

The elevator is controlled using a Finite State Machine consisting of four states.

              +------------------+
              |  IDLE_FLOOR1     |
              +------------------+
                      |
                 UP Button
                      |
                      V
              +------------------+
              |  MOVING_UP       |
              +------------------+
                      |
                      V
              +------------------+
              |  IDLE_FLOOR2     |
              +------------------+
                      |
                DOWN Button
                      |
                      V
              +------------------+
              | MOVING_DOWN      |
              +------------------+
                      |
                      V
              +------------------+
              | IDLE_FLOOR1      |
              +------------------+


# State Transition Table

| Current State | Input | Next State |
|---------------|-------|------------|
| IDLE_FLOOR1 | UP | MOVING_UP |
| MOVING_UP | Complete | IDLE_FLOOR2 |
| IDLE_FLOOR2 | DOWN | MOVING_DOWN |
| MOVING_DOWN | Complete | IDLE_FLOOR1 |
| Any State | RESET | IDLE_FLOOR1 |

---

# Working Principle

1. System starts at Floor 1.

2. LED0 is ON.

3. User presses UP button.

4. FSM enters MOVING_UP state.

5. Elevator reaches Floor 2.

6. LED1 turns ON.

7. User presses DOWN button.

8. FSM enters MOVING_DOWN state.

9. Elevator returns to Floor 1.

10. RESET button returns the system to its initial state.

---

# LED Indication

| LED | Status |
|------|--------|
| LED0 | Elevator at Floor 1 |
| LED1 | Elevator at Floor 2 |

---

# Inputs

| Input | Function |
|--------|----------|
| UP Button | Move Elevator Up |
| DOWN Button | Move Elevator Down |
| RESET | Reset System |

---

# Technologies Used

- Verilog HDL
- FPGA
- AMD Spartan-7
- Xilinx Vivado
- RTL Design
- Finite State Machine
- Digital Logic Design
- Embedded Systems

---

# Vivado Design Flow

Verilog Code
      │
      ▼
Behavioral Simulation
      │
      ▼
RTL Analysis
      │
      ▼
Synthesis
      │
      ▼
Implementation
      │
      ▼
Bitstream Generation
      │
      ▼
FPGA Programming

# Simulation Results

The design was successfully simulated in Vivado.

The following functionality was verified:

- Reset operation
- UP button operation
- DOWN button operation
- LED outputs
- FSM state transitions


# Hardware Implementation

The project was successfully implemented on the AMD Spartan-7 FPGA board.

The hardware verification includes:

- Floor 1 indication
- Floor 2 indication
- RTL schematic
- Package pin assignment
- Generated waveform

# Applications

- Elevator Control Systems
- FPGA Learning
- Digital System Design
- Embedded Systems
- FSM Demonstration
- Educational Projects
- Hardware Prototyping

# Future Improvements

- Multi-floor elevator support
- Seven-segment display
- LCD/OLED display
- Door opening and closing mechanism
- Motor driver integration
- Emergency stop button
- Overload detection
- Elevator scheduling algorithm
- Multiple elevator support
- Voice announcement system
- UART communication
- Bluetooth/Wi-Fi monitoring


# Learning Outcomes

Through this project, the following concepts were implemented and verified:

- Verilog HDL Programming
- FPGA Programming
- RTL Design
- FSM Design
- Sequential Logic Design
- Combinational Logic Design
- Xilinx Vivado Workflow
- Hardware Debugging
- FPGA Synthesis
- FPGA Implementation


# Author
Devashree Surve

Electronics Engineering (VLSI Design & Technology)

Shah & Anchor Kutchhi Engineering College

Mumbai, India

