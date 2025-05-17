<p align="center">
  <img src="Images/Top_Background.PNG" alt="Top Background" width="750"/>
</p>

# ISCAS 2025 Live Demonstration: Smart Watchdog Mechanism for Real time Fault Detection in RISC-V

[![](https://img.shields.io/badge/IEEE--Paper-blue)](https://ieeexplore.ieee.org/) 
[![](https://img.shields.io/badge/IEEE--Live--Demo--Paper-blue)](https://ieeexplore.ieee.org/) 
[![](https://img.shields.io/badge/Slides-yellow)](/Paper/) 
[![](https://img.shields.io/badge/Poster-red)](/Poster/)

This live demonstration relates to our paper titled “Smart Watchdog Mechanism for Fault Detection in RISC-V” also presented at ISCAS 2025.

Link to IEEE papers available soon with proceedings!

# Summary

In this paper we developed a novel, smarter watchdog paradigm for RISC-V processors capable of detecting control flow errors in real time. Inspired by how the human brain can perform complex computation both efficiently and reliably, we leverage Spiking Neural Networks (SNNs) as the critical decision-making element with the objective of realising a more dependable and hardware friendly watchdog architecture.

<p align="center">
  <img src="Images/Smart_Watchdog.PNG" alt="Smart Watchdog" width="400"/>
</p>

This appears to be first instance of SNNs being used as a watchdog to detect faults/errors in a processor architecture. This repository is created to support the live demonstration at ISCAS 2025, which showcases the smart watchdog delpoyed on FPGA hardware monitoring a RISC-V softcore (Neorv32) running a realisitic motor control task.

# What is a Smart Watchdog? 

When a software program is written for an embedded processors (e.g. C, or assembly), compliation toolchains convert this high level code into a sequence of instructions. The CPU then fetches instructions dynamically to execute the program algorithm. Transient faults such as Single Event Upsets (SEUs) can corrupt this sequence of instruction executed, causing the processor to deviate away from the correct program flow. This is known as a Control Flow Error (CFE).

A watchdog is an independant hardware component that monitors the execution of a software program during runtime, and can detect when CFEs occur. We call this a smart watchdog as it uses a brain-like circuit (SNN) that can be trained to make decisions on program execution based on a training process. The diagram below shows the smart watchdog implemented in hardware, and monitoring the RISC-V processor (Neorv32).

<p align="center">
  <img src="Images/Smart_Watchdog_Hardware_Implementation.PNG" alt="Smart Watchdog Hardware Implementation" width="550"/>
</p>

A methodology detailing the stages of developing this smart watchdog can be found [here](/Methodology/README.md).

# Live Demonstration of Smart Watchdog 🚀

This live demonstration showcases the smart watchdog hardware model monitoring execution Neorv32 in real time. 

# Contact

Feel free to reach out via email: simpson-d12@ulster.ac.uk

Or connect on LinkedIn: https://www.linkedin.com/in/david-simpson-040189221/

# Citation

include citation details
