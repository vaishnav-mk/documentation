---
title: LinearFunctionsToPermutations
description: API reference for qiskit.transpiler.passes.LinearFunctionsToPermutations
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.transpiler.passes.LinearFunctionsToPermutations
---

# LinearFunctionsToPermutations

<span id="qiskit.transpiler.passes.LinearFunctionsToPermutations" />

`qiskit.transpiler.passes.LinearFunctionsToPermutations(*args, **kwargs)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.25/qiskit/transpiler/passes/synthesis/linear_functions_synthesis.py "view source code")

Bases: [`TransformationPass`](qiskit.transpiler.TransformationPass "qiskit.transpiler.basepasses.TransformationPass")

Promotes linear functions to permutations when possible.

## Attributes

<span id="qiskit.transpiler.passes.LinearFunctionsToPermutations.is_analysis_pass" />

### is\_analysis\_pass

Check if the pass is an analysis pass.

If the pass is an AnalysisPass, that means that the pass can analyze the DAG and write the results of that analysis in the property set. Modifications on the DAG are not allowed by this kind of pass.

<span id="qiskit.transpiler.passes.LinearFunctionsToPermutations.is_transformation_pass" />

### is\_transformation\_pass

Check if the pass is a transformation pass.

If the pass is a TransformationPass, that means that the pass can manipulate the DAG, but cannot modify the property set (but it can be read).

## Methods

### name

<span id="qiskit.transpiler.passes.LinearFunctionsToPermutations.name" />

`name()`

Return the name of the pass.

### run

<span id="qiskit.transpiler.passes.LinearFunctionsToPermutations.run" />

`run(dag)`

Run the LinearFunctionsToPermutations pass on dag. :param dag: input dag.

**Returns**

Output dag with LinearFunctions synthesized.

**Return type**

[*DAGCircuit*](qiskit.dagcircuit.DAGCircuit "qiskit.dagcircuit.dagcircuit.DAGCircuit")

