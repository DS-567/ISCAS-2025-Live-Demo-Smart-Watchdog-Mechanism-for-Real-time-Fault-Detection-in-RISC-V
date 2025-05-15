# ISCAS 2025 Live Demonstration: Smart Watchdog Mechanism for Real time Fault Detection in RISC-V

This live demonstration relates to our paper titled “Smart Watchdog Mechanism for Fault Detection in RISC-V” also presented at ISCAS 2025. Presentation slides and poster can be viewed in **slides link** and **poster link**. Links to both the main and live demo papers will be provided here after processings are available. 

# Summary
<p align="justify">
In this paper we developed a novel, smarter watchdog paradigm for RISC-V processors capable of detecting control flow errors in real time. Inspired by how the human brain can perform complex computation both efficiently and reliably, we leverage Spiking Neural Networks (SNNs) as the critical decision-making element with the objective of realising a more dependable and hardware friendly watchdog architecture.

This appears to be first instance of SNNs being used as a watchdog to detect faults/errors in a processing architecture. This repository is created to present this work and provide more detail the smart watchdog that was developed. The live demonstration at ISCAS showcases the smart watchdog delpoyed on FPGA hardware monitoring a RISC-V softcore (Neorv32) running a realisitic motor control task.
</p>
# What is a Watchdog? 

When a software program is written (e.g. C, assembly), compliation tools convert this high level code into a sequence of instructions. The CPU then fetches instructions dynamically to realise the program algorithm. Transient faults such as Single Event Upsets (SEUs) can corrupt this instruction sequence, causing the program to be executed incorrectly. This is known as a Control Flow Error (CFE).

A watchdog is an independant hardware component that monitors the execution of a software program during runtime, and can detect when CFEs occur. This smart watchdog uses a SNN to make decisions on program execution based on an offline training process. The methodology of how the smart watchdog was developed can be found **here**.

# Live Demonstration of Smart Watchdog

# Citation

include citation details
