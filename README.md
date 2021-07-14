# SWAP-test
An  illustrative guide to implement quantum SWAP test using Qiskit.

#### The Swap test is a simple quantum circuit which, given two states, allows to compute how much do they differ from each other.

This tutorial will try to cover the following sub-tasks:
<ol>
<li>Build a variational circuit which generates the most general 1 qubit state (any point in the Bloch sphere can be reached). 
<li>Using the circuit (built in step 1) and the SWAP test, find the best choice of parameters to reproduce a randomly generated quantum state made with 1 qubit.
<li>Generalize the SWAP test for a random N-qubit product state (each of the qubits are in the state |0> or |1>). For example, the state
|a> = |01>
Is a product state, while the state
|b> = |00> + |11>
Is not.
<li>Perform a qubit by qubit SWAP test to reconstruct the state. This part of the problem can be solved via a simple grid search.
</ol>


swap_test_state_solver.py : Python script contains the helper functions for state creation, SWAP testing and state recreation.

swap_test.ipynb : An extensive demo of the functions and methodology of the different approaches used to solve the sub-tasks.
