---
title: EstimatorResult
description: API reference for qiskit.primitives.EstimatorResult
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.primitives.EstimatorResult
---

# EstimatorResult

<span id="qiskit.primitives.EstimatorResult" />

`EstimatorResult(values, metadata)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.20/qiskit/primitives/estimator_result.py "view source code")

Bases: `object`

Result of Estimator

```python
result = estimator(circuits, observables, params)
```

where the i-th elements of `result` correspond to the circuit and observable given by `circuit_indices[i]`, `observable_indices[i]`, and the parameter\_values bounds by `params[i]`. For example, `results.values[i]` gives the expectation value, and `result.metadata[i]` is a metadata dictionary for this circuit and parameters.

**Parameters**

*   **values** (*np.ndarray*) – the array of the expectation values.
*   **metadata** (*list\[dict]*) – list of the metadata.

