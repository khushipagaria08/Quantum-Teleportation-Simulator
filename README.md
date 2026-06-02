# Quantum Teleportation Simulator

## Overview

This project implements the Quantum Teleportation Protocol using Qiskit and Google Colab.

Quantum teleportation is one of the most fundamental protocols in quantum information science. It allows the quantum state of a qubit to be transferred from one location to another using quantum entanglement and classical communication.

Contrary to its name, quantum teleportation does not transport matter or energy. Instead, it transfers quantum information.

This project was built as part of my exploration of quantum computing and quantum communication concepts.

---

## Learning Objectives

Through this project, I explored:

* Qubits and quantum states
* Superposition using the Hadamard gate
* Entanglement using CNOT gates
* Bell states
* Quantum measurement
* Classical communication in quantum systems
* State reconstruction using X and Z correction gates

---

## Quantum Teleportation Protocol

The protocol uses three qubits:

| Qubit | Description                            |
| ----- | -------------------------------------- |
| Q     | Unknown quantum state to be teleported |
| A     | Alice's entangled qubit                |
| B     | Bob's entangled qubit                  |

### Step 1: Create Entanglement

A Bell pair is created between Alice's qubit (A) and Bob's qubit (B):

(|00⟩ + |11⟩)/√2

This shared entangled state acts as the quantum channel.

### Step 2: Prepare the State to Teleport

An arbitrary quantum state is prepared on qubit Q:

ψ = α|0⟩ + β|1⟩

### Step 3: Entangle Q with Alice's Qubit

A CNOT gate followed by a Hadamard gate is applied.

These operations distribute the information of the unknown state across the three-qubit system.

### Step 4: Measurement

Alice measures her two qubits and obtains one of four outcomes:

* 00
* 01
* 10
* 11

These two classical bits are sent to Bob.

### Step 5: State Reconstruction

Depending on Alice's measurement result, Bob applies correction gates:

| Measurement | Correction |
| ----------- | ---------- |
| 00          | None       |
| 01          | X          |
| 10          | Z          |
| 11          | X + Z      |

After the correction, Bob's qubit becomes:

ψ = α|0⟩ + β|1⟩

which is exactly the original state.

---

## Circuit

<img width="392" height="213" alt="image" src="https://github.com/user-attachments/assets/48d5778e-91bd-4179-8dd5-65acbfe43301" />


---

## Results

The simulator successfully demonstrates quantum teleportation by transferring the state of qubit Q to Bob's qubit B.

The histogram shows the distribution of Alice's measurement outcomes (00, 01, 10, and 11). Based on the outcome received, Bob applies the appropriate correction gate(s) (X and/or Z) to reconstruct the original quantum state.
<img width="794" height="587" alt="image" src="https://github.com/user-attachments/assets/eb365063-b53a-49a9-882b-324873666c16" />

---

## Technologies Used

* Python
* Qiskit
* Qiskit Aer
* Google Colab
* Matplotlib

---


## Author

Khushi Pagaria

