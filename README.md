# SWAP-test - single and multi-qubit SWAP test using Qiskit
Dependencies:

I have tried to use very few dependencies and tried to define the elementary functions myself.

[Qiskit](https://qiskit.org/documentation/getting_started.html) (with visualization support) is the only dependency. To install it - 
```
pip install qiskit[visualization]
```
<hr>

#### The [Swap test](https://en.wikipedia.org/wiki/Swap_test) is a simple quantum circuit which, given two states, allows to compute how much do they differ from each other.

SWAP test is a classic example in quantum computing which can be used as base example to get acquainted with various functionalities in qiskit. This [notebook](swap_test.ipynb) uses some utility functions defined in [swap_test_state_solver.py](swap_test_state_solver.py) to avoid much cluttering, I have tried to keep enough docstrings for each function and hope that other will find it useful. 

Swap test is one of the simpler concepts and can be a good way to get started with Qiskit. I have tried my best to provide images with annotations for better explanation as I struggled when I was learning it due to lack of visualizations.

This project will try to cover the following sub-tasks:
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

<hr>
Contents:

swap_test.ipynb : An extensive demo of the functions and methodology of the different approaches used to solve the sub-tasks.
swap_test_state_solver.py : Python script contains the helper functions for state creation, SWAP testing and state recreation.

<hr>

Some good resources for SWAP test:

[Wiki](https://en.wikipedia.org/wiki/Swap_test)<br />
[Basis specific swap test](https://bsiegelwax.medium.com/basis-specific-swap-test-comparing-quantum-states-2cce0fb379de)<br />
[Multi-qubit swap test](https://quantumcomputing.stackexchange.com/questions/9775/swap-test-to-calculate-inner-product-with-qiskit-for-multi-qubit-states)
