# ISCAS 2025 Live Demonstration: Smart Watchdog Mechanism for Real time Fault Detection in RISC-V

This live demonstration relates to our paper titled “Smart Watchdog Mechanism for Fault Detection in RISC-V” also presented at ISCAS 2025. Presentation slides and poster can be viewed here: [Slides](/Paper) and [Poster](/Poster)

Link to main paper: Available soon with proceedings!

Link to live demo paper: Available soon with proceedings!

# Summary

In this paper we developed a novel, smarter watchdog paradigm for RISC-V processors capable of detecting control flow errors in real time. Inspired by how the human brain can perform complex computation both efficiently and reliably, we leverage Spiking Neural Networks (SNNs) as the critical decision-making element with the objective of realising a more dependable and hardware friendly watchdog architecture.


<p align="center">
  <img src="Images/Smart_Watchdog.PNG" alt="Smart Watchdog" width="400"/>
</p>
This appears to be first instance of SNNs being used as a watchdog to detect faults/errors in a processing architecture. This repository is created to present this work and provide more detail the smart watchdog that was developed. The live demonstration at ISCAS showcases the smart watchdog delpoyed on FPGA hardware monitoring a RISC-V softcore (Neorv32) running a realisitic motor control task.

# What is a Smart Watchdog? 

When a software program is written for an embedded processors (e.g. in C, or assembly), compliation toolchains convert this high level code into a sequence of instructions. The CPU then fetches instructions dynamically to execute the program algorithm. Transient faults such as Single Event Upsets (SEUs) can corrupt this sequence of instruction executed, causing the processor to deviate away from the correct program flow. This is known as a Control Flow Error (CFE).

A watchdog is an independant hardware component that monitors the execution of a software program during runtime, and can detect when CFEs occur. We call this a smart watchdog as it uses a brain-like circuit (SNN) that can be trained to make decisions on program execution based on a training process.

A methodology detailing the stages of developing this smart watchdog can be found [here](/Methodology/README.md).

# Live Demonstration of Smart Watchdog

This live demonstration 

# Citation

include citation details
