# Week 4 Tasks

This folder contains the completed Week 4 tasks in Qiskit.

## Files

- `Week4_tasks.ipynb`: notebook containing the three completed tasks
- `my_random_circuit.qasm`: hand-written QASM file used in Task 3

## Summary of work

### Task 1: Q-sphere with a 90 degree phase difference

A 2-qubit circuit was created using:

- `H` on qubit 0
- `H` on qubit 1
- `S` on qubit 1

This creates a two-qubit superposition with a 90 degree phase shift on part of the state.

The Q-sphere result shows:

- all four basis states are present
- all four basis states have equal probability
- `|10⟩` and `|11⟩` have a different phase colour from `|00⟩` and `|01⟩`

This shows that the circuit changes relative phase without changing the overall probability distribution.

### Task 2: Density matrix of the same circuit

The same circuit from Task 1 was converted into a density matrix and visualised using the state-city plot.

The result shows:

- diagonal elements are all `0.25`, so each basis state has probability `1/4`
- off-diagonal elements are non-zero, showing coherence between basis states
- imaginary off-diagonal terms appear because the `S` gate introduced a 90 degree phase shift

This shows that the density matrix contains more information than measurement probabilities alone.

### Task 3: Hand-written QASM circuit

A separate circuit was written manually in `my_random_circuit.qasm` without using the `dump` method.

The QASM file was then loaded into Qiskit, printed, and executed.

The circuit uses only gates already seen in the course materials:

- `h`
- `x`
- `s`
- `cx`
- `measure`

The execution result gives valid measurement counts, showing that the hand-written QASM file can be loaded and run successfully.

## Notes

- `my_random_circuit.qasm` keeps `include "qelib1.inc";` for Qiskit.
- In some other environments, that include line may need to be removed.
