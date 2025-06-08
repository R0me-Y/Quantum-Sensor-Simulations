# Qubit Phase Damping Simulation

This repository contains a Wolfram Language (Mathematica) script that simulates the effect of phase damping on a qubit's density matrix. The simulation observes the decay of the off-diagonal element (coherence) of the density matrix, which is a key indicator of decoherence.

## Objective

The primary objectives of this simulation are to:
- Simulate the effect of phase damping on a qubit's density matrix.
- Observe the decay of the off-diagonal element (coherence) over time.

## Theoretical Background

**Phase Damping** is a quantum noise channel that causes loss of phase information without energy loss. Physically, it corresponds to random fluctuations in the qubit's energy levels, leading to dephasing.

The density matrix \(\rho\) evolves under the quantum channel via the **Kraus operators** \(K_i\):

\[
\rho(t) = \sum_i K_i \rho(0) K_i^\dagger
\]

For phase damping, the Kraus operators are:

\[
K_0 = \begin{pmatrix} 1 & 0 \\ 0 & \sqrt{1-p} \end{pmatrix}, \quad
K_1 = \begin{pmatrix} 0 & 0 \\ 0 & \sqrt{p} \end{pmatrix}
\]

where \(p\) is the probability of phase flip, related to time \(t\) and damping rate \(\gamma\) by:

\[
p = 1 - e^{-\gamma t}
\]

The coherence of the qubit is represented by the off-diagonal element \(|\rho_{01}|\), which decays exponentially under phase damping.

## Project Structure

The core simulation is contained within a single Wolfram Language notebook (`.nb`) or script (`.wl`), which:
- Defines the initial qubit state and density matrix.
- Implements the Kraus operators for phase damping.
- Evolves the density matrix over time.
- Extracts and plots the coherence decay.

## How to Run

1. **Prerequisites:** Wolfram Mathematica installed on your system.
2. **Clone the Repository:**  
   Replace the URL below with this repository's actual URL.
   ```bash
   git clone https://github.com/your-username/qubit-phase-damping.git
   cd qubit-phase-damping
