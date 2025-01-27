---
title: EquivalenceLibrary
description: API reference for qiskit.circuit.EquivalenceLibrary
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.circuit.EquivalenceLibrary
---

# EquivalenceLibrary

<span id="qiskit.circuit.EquivalenceLibrary" />

`EquivalenceLibrary(*, base=None)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/circuit/equivalence.py "view source code")

Bases: `object`

A library providing a one-way mapping of Gates to their equivalent implementations as QuantumCircuits.

Create a new equivalence library.

**Parameters**

**base** (*Optional\[*[*EquivalenceLibrary*](#qiskit.circuit.EquivalenceLibrary "qiskit.circuit.EquivalenceLibrary")*]*) – Base equivalence library to be referenced if an entry is not found in this library.

## Methods

<span id="qiskit-circuit-equivalencelibrary-add-equivalence" />

### add\_equivalence

<span id="qiskit.circuit.EquivalenceLibrary.add_equivalence" />

`EquivalenceLibrary.add_equivalence(gate, equivalent_circuit)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/circuit/equivalence.py "view source code")

Add a new equivalence to the library. Future queries for the Gate will include the given circuit, in addition to all existing equivalences (including those from base).

Parameterized Gates (those including qiskit.circuit.Parameters in their Gate.params) can be marked equivalent to parameterized circuits, provided the parameters match.

**Parameters**

*   **gate** ([*Gate*](qiskit.circuit.Gate "qiskit.circuit.Gate")) – A Gate instance.
*   **equivalent\_circuit** ([*QuantumCircuit*](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")) – A circuit equivalently implementing the given Gate.

<span id="qiskit-circuit-equivalencelibrary-draw" />

### draw

<span id="qiskit.circuit.EquivalenceLibrary.draw" />

`EquivalenceLibrary.draw(filename=None)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/circuit/equivalence.py "view source code")

Draws the equivalence relations available in the library.

**Parameters**

**filename** (*str*) – An optional path to write the output image to if specified this method will return None.

**Returns**

**Drawn equivalence library as an**

IPython SVG if in a jupyter notebook, or as a PIL.Image otherwise.

**Return type**

PIL.Image or IPython.display.SVG

**Raises**

**InvalidFileError** – if filename is not valid.

<span id="qiskit-circuit-equivalencelibrary-get-entry" />

### get\_entry

<span id="qiskit.circuit.EquivalenceLibrary.get_entry" />

`EquivalenceLibrary.get_entry(gate)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/circuit/equivalence.py "view source code")

Gets the set of QuantumCircuits circuits from the library which equivalently implement the given Gate.

Parameterized circuits will have their parameters replaced with the corresponding entries from Gate.params.

**Parameters**

**gate** ([*Gate*](qiskit.circuit.Gate "qiskit.circuit.Gate")) – A Gate instance.

**Returns**

**A list of equivalent QuantumCircuits. If empty,**

library contains no known decompositions of Gate.

Returned circuits will be ordered according to their insertion in the library, from earliest to latest, from top to base. The ordering of the StandardEquivalenceLibrary will not generally be consistent across Qiskit versions.

**Return type**

List\[[QuantumCircuit](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")]

<span id="qiskit-circuit-equivalencelibrary-has-entry" />

### has\_entry

<span id="qiskit.circuit.EquivalenceLibrary.has_entry" />

`EquivalenceLibrary.has_entry(gate)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/circuit/equivalence.py "view source code")

Check if a library contains any decompositions for gate.

**Parameters**

**gate** ([*Gate*](qiskit.circuit.Gate "qiskit.circuit.Gate")) – A Gate instance.

**Returns**

**True if gate has a known decomposition in the library.**

False otherwise.

**Return type**

Bool

<span id="qiskit-circuit-equivalencelibrary-keys" />

### keys

<span id="qiskit.circuit.EquivalenceLibrary.keys" />

`EquivalenceLibrary.keys()`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/circuit/equivalence.py "view source code")

Return list of keys to key to node index map.

**Returns**

Keys to the key to node index map.

**Return type**

List

<span id="qiskit-circuit-equivalencelibrary-node-index" />

### node\_index

<span id="qiskit.circuit.EquivalenceLibrary.node_index" />

`EquivalenceLibrary.node_index(key)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/circuit/equivalence.py "view source code")

Return node index for a given key.

**Parameters**

**key** (*Key*) – Key to an equivalence.

**Returns**

Index to the node in the graph for the given key.

**Return type**

Int

<span id="qiskit-circuit-equivalencelibrary-set-entry" />

### set\_entry

<span id="qiskit.circuit.EquivalenceLibrary.set_entry" />

`EquivalenceLibrary.set_entry(gate, entry)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/circuit/equivalence.py "view source code")

Set the equivalence record for a Gate. Future queries for the Gate will return only the circuits provided.

Parameterized Gates (those including qiskit.circuit.Parameters in their Gate.params) can be marked equivalent to parameterized circuits, provided the parameters match.

**Parameters**

*   **gate** ([*Gate*](qiskit.circuit.Gate "qiskit.circuit.Gate")) – A Gate instance.
*   **entry** (*List\['QuantumCircuit']*) – A list of QuantumCircuits, each equivalently implementing the given Gate.

## Attributes

<span id="qiskit.circuit.EquivalenceLibrary.graph" />

### graph

Return graph representing the equivalence library data.

This property should be treated as read-only as it provides a reference to the internal state of the [`EquivalenceLibrary`](#qiskit.circuit.EquivalenceLibrary "qiskit.circuit.EquivalenceLibrary") object. If the graph returned by this property is mutated it could corrupt the the contents of the object. If you need to modify the output `PyDiGraph` be sure to make a copy prior to any modification.

**Returns**

A graph object with equivalence data in each node.

**Return type**

PyDiGraph

