---
title: dag_to_circuit
description: API reference for qiskit.converters.dag_to_circuit
in_page_toc_min_heading_level: 1
python_api_type: function
python_api_name: qiskit.converters.dag_to_circuit
---

# qiskit.converters.dag\_to\_circuit

<span id="qiskit.converters.dag_to_circuit" />

`dag_to_circuit(dag)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.23/qiskit/converters/dag_to_circuit.py "view source code")

Build a `QuantumCircuit` object from a `DAGCircuit`.

**Parameters**

**dag** ([*DAGCircuit*](qiskit.dagcircuit.DAGCircuit "qiskit.dagcircuit.DAGCircuit")) – the input dag.

**Returns**

the circuit representing the input dag.

**Return type**

[QuantumCircuit](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")

## Example

```python
from qiskit import QuantumRegister, ClassicalRegister, QuantumCircuit
from qiskit.dagcircuit import DAGCircuit
from qiskit.converters import circuit_to_dag
from qiskit.circuit.library.standard_gates import CHGate, U2Gate, CXGate
from qiskit.converters import dag_to_circuit

q = QuantumRegister(3, 'q')
c = ClassicalRegister(3, 'c')
circ = QuantumCircuit(q, c)
circ.h(q[0])
circ.cx(q[0], q[1])
circ.measure(q[0], c[0])
circ.rz(0.5, q[1]).c_if(c, 2)
dag = circuit_to_dag(circ)
circuit = dag_to_circuit(dag)
circuit.draw('mpl')
```

([Source code](qiskit-converters-dag_to_circuit-1.py), [png](qiskit-converters-dag_to_circuit-1.png), [hires.png](qiskit-converters-dag_to_circuit-1.hires.png), [pdf](qiskit-converters-dag_to_circuit-1.pdf))

![../\_images/qiskit-converters-dag\_to\_circuit-1.png](/images/api/qiskit/0.40/qiskit-converters-dag_to_circuit-1.png)

