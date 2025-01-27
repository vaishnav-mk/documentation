---
title: ADMMOptimizer
description: API reference for qiskit.optimization.algorithms.ADMMOptimizer
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.optimization.algorithms.ADMMOptimizer
---

# ADMMOptimizer

<span id="qiskit.optimization.algorithms.ADMMOptimizer" />

`ADMMOptimizer(qubo_optimizer=None, continuous_optimizer=None, params=None)`[GitHub](https://github.com/qiskit-community/qiskit-aqua/tree/stable/0.9/qiskit/optimization/algorithms/admm_optimizer.py "view source code")

Bases: `qiskit.optimization.algorithms.optimization_algorithm.OptimizationAlgorithm`

An implementation of the ADMM-based heuristic.

This algorithm is introduced in \[1].

**References:**

**\[1] Gambella, C., & Simonetto, A. (2020). Multi-block ADMM Heuristics for Mixed-Binary**

Optimization on Classical and Quantum Computers. arXiv preprint arXiv:2001.02069.

**Parameters**

*   **qubo\_optimizer** (`Optional`\[`OptimizationAlgorithm`]) – An instance of OptimizationAlgorithm that can effectively solve QUBO problems. If not specified then [`MinimumEigenOptimizer`](qiskit.optimization.algorithms.MinimumEigenOptimizer "qiskit.optimization.algorithms.MinimumEigenOptimizer") initialized with an instance of `NumPyMinimumEigensolver` will be used.
*   **continuous\_optimizer** (`Optional`\[`OptimizationAlgorithm`]) – An instance of OptimizationAlgorithm that can solve continuous problems. If not specified then [`SlsqpOptimizer`](qiskit.optimization.algorithms.SlsqpOptimizer "qiskit.optimization.algorithms.SlsqpOptimizer") will be used.
*   **params** (`Optional`\[`ADMMParameters`]) – An instance of ADMMParameters.

## Methods

### get\_compatibility\_msg

<span id="qiskit.optimization.algorithms.ADMMOptimizer.get_compatibility_msg" />

`ADMMOptimizer.get_compatibility_msg(problem)`[GitHub](https://github.com/qiskit-community/qiskit-aqua/tree/stable/0.9/qiskit/optimization/algorithms/admm_optimizer.py "view source code")

Checks whether a given problem can be solved with the optimizer implementing this method.

**Parameters**

**problem** (`QuadraticProgram`) – The optimization problem to check compatibility.

**Return type**

`Optional`\[`str`]

**Returns**

Returns True if the problem is compatible, otherwise raises an error.

**Raises**

[**QiskitOptimizationError**](qiskit.optimization.QiskitOptimizationError "qiskit.optimization.QiskitOptimizationError") – If the problem is not compatible with the ADMM optimizer.

### is\_compatible

<span id="qiskit.optimization.algorithms.ADMMOptimizer.is_compatible" />

`ADMMOptimizer.is_compatible(problem)`

Checks whether a given problem can be solved with the optimizer implementing this method.

**Parameters**

**problem** (`QuadraticProgram`) – The optimization problem to check compatibility.

**Return type**

`bool`

**Returns**

Returns True if the problem is compatible, False otherwise.

### solve

<span id="qiskit.optimization.algorithms.ADMMOptimizer.solve" />

`ADMMOptimizer.solve(problem)`[GitHub](https://github.com/qiskit-community/qiskit-aqua/tree/stable/0.9/qiskit/optimization/algorithms/admm_optimizer.py "view source code")

Tries to solves the given problem using ADMM algorithm.

**Parameters**

**problem** (`QuadraticProgram`) – The problem to be solved.

**Return type**

`ADMMOptimizationResult`

**Returns**

The result of the optimizer applied to the problem.

**Raises**

[**QiskitOptimizationError**](qiskit.optimization.QiskitOptimizationError "qiskit.optimization.QiskitOptimizationError") – If the problem is not compatible with the ADMM optimizer.

## Attributes

<span id="qiskit.optimization.algorithms.ADMMOptimizer.parameters" />

### parameters

Returns current parameters of the optimizer.

**Return type**

`ADMMParameters`

**Returns**

The parameters.

