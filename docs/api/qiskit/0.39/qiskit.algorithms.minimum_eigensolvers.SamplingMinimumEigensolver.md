---
title: SamplingMinimumEigensolver
description: API reference for qiskit.algorithms.minimum_eigensolvers.SamplingMinimumEigensolver
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.algorithms.minimum_eigensolvers.SamplingMinimumEigensolver
---

# SamplingMinimumEigensolver

<span id="qiskit.algorithms.minimum_eigensolvers.SamplingMinimumEigensolver" />

`SamplingMinimumEigensolver`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.22/qiskit/algorithms/minimum_eigensolvers/sampling_mes.py "view source code")

Bases: `abc.ABC`

The Sampling Minimum Eigensolver Interface.

## Methods

### compute\_minimum\_eigenvalue

<span id="qiskit.algorithms.minimum_eigensolvers.SamplingMinimumEigensolver.compute_minimum_eigenvalue" />

`abstract SamplingMinimumEigensolver.compute_minimum_eigenvalue(operator, aux_operators=None)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.22/qiskit/algorithms/minimum_eigensolvers/sampling_mes.py "view source code")

Compute the minimum eigenvalue of a diagonal operator.

**Parameters**

*   **operator** (*BaseOperator |* [*PauliSumOp*](qiskit.opflow.primitive_ops.PauliSumOp "qiskit.opflow.primitive_ops.PauliSumOp")) – Diagonal qubit operator.
*   **aux\_operators** (*ListOrDict\[BaseOperator |* [*PauliSumOp*](qiskit.opflow.primitive_ops.PauliSumOp "qiskit.opflow.primitive_ops.PauliSumOp")*] | None*) – Optional list of auxiliary operators to be evaluated with the final state.

**Return type**

[SamplingMinimumEigensolverResult](qiskit.algorithms.minimum_eigensolvers.SamplingMinimumEigensolverResult "qiskit.algorithms.minimum_eigensolvers.SamplingMinimumEigensolverResult")

**Returns**

A [`SamplingMinimumEigensolverResult`](qiskit.algorithms.minimum_eigensolvers.SamplingMinimumEigensolverResult "qiskit.algorithms.minimum_eigensolvers.SamplingMinimumEigensolverResult") containing the optimization result.

### supports\_aux\_operators

<span id="qiskit.algorithms.minimum_eigensolvers.SamplingMinimumEigensolver.supports_aux_operators" />

`classmethod SamplingMinimumEigensolver.supports_aux_operators()`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.22/qiskit/algorithms/minimum_eigensolvers/sampling_mes.py "view source code")

Whether computing the expectation value of auxiliary operators is supported.

If the minimum eigensolver computes an eigenstate of the main operator then it can compute the expectation value of the aux\_operators for that state. Otherwise they will be ignored.

**Return type**

`bool`

**Returns**

True if aux\_operator expectations can be evaluated, False otherwise

