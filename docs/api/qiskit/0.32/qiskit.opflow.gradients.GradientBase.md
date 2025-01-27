---
title: GradientBase
description: API reference for qiskit.opflow.gradients.GradientBase
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.opflow.gradients.GradientBase
---

# GradientBase

<span id="qiskit.opflow.gradients.GradientBase" />

`GradientBase(grad_method='param_shift', **kwargs)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.18/qiskit/opflow/gradients/gradient_base.py "view source code")

Bases: `qiskit.opflow.gradients.derivative_base.DerivativeBase`

Base class for first-order operator gradient.

Convert an operator expression to the first-order gradient.

**Parameters**

*   **grad\_method** (`Union`\[`str`, `CircuitGradient`]) – The method used to compute the state/probability gradient. Can be either `'param_shift'` or `'lin_comb'` or `'fin_diff'`. Ignored for gradients w\.r.t observable parameters.
*   **kwargs** (*dict*) – Optional parameters for a CircuitGradient

**Raises**

**ValueError** – If method != `fin_diff` and `epsilon` is not None.

## Attributes

<span id="qiskit.opflow.gradients.GradientBase.grad_method" />

### grad\_method

Returns `CircuitGradient`.

**Return type**

`CircuitGradient`

**Returns**

`CircuitGradient`.

