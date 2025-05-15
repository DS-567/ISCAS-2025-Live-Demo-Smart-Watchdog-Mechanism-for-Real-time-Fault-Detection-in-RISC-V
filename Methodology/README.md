# Methodology

There were 8 stages to develop the smart watchdog, as shown below. This information can also be found in the main paper.

<p align="center">
  <img src="../Images/Methodology.PNG" alt="Methodology" width="900"/>
</p>

## **Stage 1 - Data Collection**:

A custom hardware framework was developed to inject faults into RISC-V core and extract instruction data to text files, creating a library of instructions executed normally and with control flow errors occuring. (Hardware architecture will be discussed in a future publication).

Three different software applications were executed on Neorv32:
* **Fibonacci Series - generates first 45 numbers.**
* **Bubble Sort - sorts 25 numbers.**
* **Matrix Multiplication - multiplies a 4x4 matrix**

Every clock cycle of execution in Neorv32, six data points are extracted:

* **Instruction Register (IR):** Defines the type of instruction being executed.
* **Program Counter Register (PC):** Holds the memory address of the instruction being executed.
* **FSM Execute Engine States:** Internal CPU states (instruction dispatch, execute, branched, trap entry etc).
* **Source Register 1 (RS1):** Source register 1 used in instructions (can hold addresses for computation).
* **Machine Trap Base Address Register (MTVEC):** Holds the base address of the trap handler (trap entry point).
* **Machine Exception Program Counter (MEPC):** Holds the return address from the trap handler (trap exit point).

Totals 164 bits of parallel input to the smart watchdog.

## **Stage 2 - Feature Extraction**:

These six data signals combined provide information on control flow in the RISC-V architecture. To allow for changes in program code (e.g. different instruction sequences), and to reduce input data width to the SNN, features are extracted as shown below. The 164 bits are condensed down to just 16 binary features, with each feature capturing a single piece of information relating to the current instruction. The goal is to train the SNN model to distinguish between normal execution and control flow errors.

<p align="center">
  <img src="../Images/Feature_Layer.PNG" alt="Feature Layer" width="600"/>
</p>

## **Stage 3 - Dataset Preprocessing**:

The data collection stage gathered around 6.7 million instructions from the RISC-V (Neorv32). As the name implies, there are a reduced number of instructions in the base RISC-V architecture. The data for each instruction in the text files from data collection is passed through feature layer (Python script), creating a binary feature dataset for each of the three applications. As many of the instructions produce the same features, only unique feature samples are appended to the dataset.

<p align="center">
  <img src="../Images/Dataset_Preprocessing.PNG" alt="Dataset Preprocessing" width="800"/>
</p>

## **Stage 4 - SNN Model Design**:

dfafagdg

## **Stage 5 - SNN Model Training**:

dfafagdg

## **Stage 6 - SNN Model Testing**:

dfafagdg

## **Stage 7 - Smart Watchdog Implementation**:

dfafagdg

## **Stage 8 - Smart Watchdog Validation**:

dfafagdg
