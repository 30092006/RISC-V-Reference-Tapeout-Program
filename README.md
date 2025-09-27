# RISC-V  SoC Tapeout Program VSD

## Tools Installation

#### <ins>All the instructions for installation of required tools can be found here:</ins>

### **System Requirements**
- 6 GB RAM
- 50 GB HDD
- Ubuntu 20.04 or higher
- 4 vCPU

### **Resizing the Ubuntu window to fit the screen**
```bash
$ sudo apt update
$ sudo apt install build-essential dkms linux-headers-$(uname -r)
$ cd /media/spatha/VBox_GAs_7.1.8/
$ ./autorun.sh
```

### **TOOL CHECK**

#### <ins>**Yosys**</ins>
```bash
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make               # If make is not installed
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
# Yosys build depends on a Git submodule called abc, which hasn't been initialized yet. You need to run the following command before running make
$ git submodule update --init --recursive
$ make 
$ sudo make install
```
![Alt Text](Images/Yosys.png)

#### <ins>**Iverilog**</ins>
```bash
$ sudo apt-get update
$ sudo apt-get install iverilog
```
![Alt Text](Images/Iverilog.png)

#### <ins>**gtkwave**</ins>
```bash
$ sudo apt-get update
$ sudo apt install gtkwave
```
![Alt Text](Images/Gtkwave.png)
Day 1: Introduction to Verilog RTL Design & Synthesis

Welcome to Day 1 of the RTL Workshop! Today marks the beginning of your journey into digital design, Verilog coding, and hardware description languages. By the end of this session, you'll be able to write simple RTL modules, simulate them, and perform basic synthesis.


---

📚 Objectives

By the end of this session, participants will be able to:

1. Understand the basics of Digital Logic Design.


2. Learn Verilog HDL syntax and coding standards.


3. Perform simulation using Icarus Verilog (iverilog).


4. Conduct RTL synthesis with Yosys.


5. Analyze timing diagrams and module behavior.




---

🛠 Tools Required

Icarus Verilog (iverilog) – Open-source Verilog simulator

Yosys – Open-source logic synthesis tool

GTKWave – Waveform viewer for simulation results

Text editor or IDE (VS Code recommended)



RTL Design Workshop: 5-Day Guide

Day 1: Introduction & Basic Verilog

Objective: Establish foundational knowledge of Verilog and RTL design.

Tasks:

1. Install Verilog simulation tools (Icarus Verilog, GTKWave).


2. Write a simple combinational circuit (2-to-1 multiplexer).


3. Create a testbench to verify functionality.


4. Simulate and observe waveforms.


5. Document challenges and observations.



Deliverable: A working multiplexer Verilog module with a verified testbench.


---

Day 2: Sequential Logic & Counters

Objective: Learn sequential design and basic timing concepts.

Tasks:

1. Design a 4-bit synchronous counter with enable and reset signals.


2. Implement a testbench with multiple scenarios:

Normal counting

Reset functionality

Enable/disable behavior



3. Simulate using waveform analyzer; verify all scenarios.


4. Add comments and timing diagrams for documentation.



Deliverable: Counter module with fully functional testbench and timing report.


---

Day 3: RTL Optimization & Modular Design

Objective: Practice writing reusable and optimized RTL modules.

Tasks:

1. Refactor the counter into a parameterized module (e.g., n-bit counter).


2. Combine multiple small modules into a top-level design (e.g., counter + decoder).


3. Optimize for minimal logic usage while keeping functionality.


4. Run simulations to ensure correctness after modular integration.


5. Record synthesis metrics like LUTs, flip-flops, and critical path delays.



Deliverable: Modular, parameterized RTL design with optimized logic utilization.


---

Day 4: RTL Synthesis & Timing Analysis

Objective: Translate RTL into gate-level design and analyze timing.

Tasks:

1. Set up synthesis flow using an open-source tool (Yosys or Vivado).


2. Synthesize the top-level design from Day 3.


3. Analyze synthesis report:

Number of gates

Maximum frequency

Propagation delay



4. Apply constraints (clock period, input/output delays) to meet timing.


5. Generate a gate-level netlist and compare simulation with RTL behavior.



Deliverable: Synthesis report, gate-level netlist, and verified timing analysis.


---

Day 5: Advanced Verification & Reporting

Objective: Verify overall design correctness and prepare professional documentation.

Tasks:

1. Develop an advanced testbench using assertions and random stimulus.


2. Check corner cases and boundary conditions.


3. Generate functional coverage reports to ensure all cases are tested.


4. Document the full workflow: RTL → Simulation → Synthesis → Verification.


5. Prepare a GitHub-ready repository with organized files, README, and diagrams.



Deliverable: Fully verified RTL project with structured GitHub repository and complete documentation.













