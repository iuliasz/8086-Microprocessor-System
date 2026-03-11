# 8086 Microprocessor-Based System

## Project Overview
This project consists of the design of a microprocessor-based system built around the Intel 8086 architecture.  
The goal is to design and integrate memory modules, input/output interfaces, and peripheral devices while implementing low-level control routines in assembly language.

The project focuses on understanding microprocessor system architecture, memory mapping, and hardware interfacing.

# System Architecture

The microsystem includes the following components:

## Central Processing Unit
- Intel 8086 microprocessor

## Memory
- **128 KB EPROM** using 27C512 memory circuits  
- **64 KB SRAM** using 62256 memory circuits  

## Interfaces
- **Serial interface:** implemented using the 8251 USART
- **Parallel interface:** implemented using the 8255 Programmable Peripheral Interface (PPI)

## Input Devices
- Mini keyboard with **9 keys**

## Output Devices
- **10 LEDs**
- **7-segment display module** with 8 digits (up to 8 hexadecimal characters)
- **LCD display module** (2 lines × 16 characters)

# Memory and I/O Mapping

## Serial Interface (8251)
Address range:

04D0H – 04D2H
or
05D0H – 05D2H

The address depends on the position of **switch S1**.

## Parallel Interface (8255)
Address range:

0250H – 0256H
or
0A50H – 0A56H

The address depends on the position of **switch S2**.

# Assembly Software Structure
All programs are implemented in **8086 assembly language** and organized as reusable subroutines.

The following routines are implemented:
- Initialization routines for **8251** and **8255**
- Serial communication routines (character transmit / receive)
- Parallel interface character output routine
- Mini-keyboard scanning routine
- LED control routines (turn on / turn off)
- 7-segment display routine for hexadecimal characters

Each routine is designed with clearly defined:
- Inputs
- Processing steps
- Outputs

# Project Phases

## 1. System Design
- Define system architecture
- Design memory and I/O mapping
- Create block diagrams for system components

## 2. Implementation
- Configure memory modules and peripheral interfaces
- Develop assembly routines for device control
- Implement keyboard input and display output functionality

## 3. Testing
- Test each assembly routine
- Verify communication with serial and parallel interfaces
- Validate keyboard input and output devices

# Learning Outcomes
Through this project the following concepts are developed:
- Understanding of **8086 microprocessor architecture**
- Low-level **assembly programming**
- Peripheral interfacing
- Memory mapping
- Embedded system design fundamentals
