---
title: ExcitedStatesEigensolver
description: API reference for qiskit.chemistry.algorithms.ExcitedStatesEigensolver
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.chemistry.algorithms.ExcitedStatesEigensolver
---

# ExcitedStatesEigensolver

<span id="qiskit.chemistry.algorithms.ExcitedStatesEigensolver" />

`ExcitedStatesEigensolver(transformation, solver)`[GitHub](https://github.com/qiskit-community/qiskit-aqua/tree/stable/0.9/qiskit/chemistry/algorithms/excited_states_solvers/excited_states_eigensolver.py "view source code")

Bases: `qiskit.chemistry.algorithms.excited_states_solvers.excited_states_solver.ExcitedStatesSolver`

The calculation of excited states via an Eigensolver algorithm

**Parameters**

*   **transformation** (`Transformation`) – Qubit Operator Transformation
*   **solver** (`Union`\[`Eigensolver`, `EigensolverFactory`]) – Minimum Eigensolver or MESFactory object.

## Methods

### solve

<span id="qiskit.chemistry.algorithms.ExcitedStatesEigensolver.solve" />

`ExcitedStatesEigensolver.solve(driver, aux_operators=None)`[GitHub](https://github.com/qiskit-community/qiskit-aqua/tree/stable/0.9/qiskit/chemistry/algorithms/excited_states_solvers/excited_states_eigensolver.py "view source code")

Compute Ground and Excited States properties.

**Parameters**

*   **driver** (`BaseDriver`) – a chemistry driver object which defines the chemical problem that is to be solved by this calculation.
*   **aux\_operators** (`Optional`\[`List`\[`Any`]]) – Additional auxiliary operators to evaluate. Must be of type `FermionicOperator` if the qubit transformation is fermionic and of type `BosonicOperator` it is bosonic.

**Raises**

**NotImplementedError** – If an operator in `aux_operators` is not of type `FermionicOperator`.

**Return type**

`Union`\[`ElectronicStructureResult`, `VibronicStructureResult`]

**Returns**

An eigenstate result. Depending on the transformation this can be an electronic structure or bosonic result.

## Attributes

<span id="qiskit.chemistry.algorithms.ExcitedStatesEigensolver.solver" />

### solver

Returns the minimum eigensolver or factory.

**Return type**

`Union`\[`Eigensolver`, `EigensolverFactory`]

<span id="qiskit.chemistry.algorithms.ExcitedStatesEigensolver.transformation" />

### transformation

Returns the transformation used to obtain a qubit operator from the molecule.

**Return type**

`Transformation`

