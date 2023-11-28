<span id="qiskit-circuit-controlledgate" />

# qiskit.circuit.ControlledGate

<span id="undefined" />

`ControlledGate(name, num_qubits, params, label=None, num_ctrl_qubits=1, definition=None, ctrl_state=None, base_gate=None)`

Controlled unitary gate.

Create a new ControlledGate. In the new gate the first `num_ctrl_qubits` of the gate are the controls.

**Parameters**

*   **name** (`str`) – The name of the gate.
*   **num\_qubits** (`int`) – The number of qubits the gate acts on.
*   **params** (`List`) – A list of parameters for the gate.
*   **label** (`Optional`\[`str`]) – An optional label for the gate.
*   **num\_ctrl\_qubits** (`Optional`\[`int`]) – Number of control qubits.
*   **definition** (`Optional`\[`QuantumCircuit`]) – A list of gate rules for implementing this gate. The elements of the list are tuples of ([`Gate()`](qiskit.circuit.Gate#qiskit.circuit.Gate "qiskit.circuit.Gate"), \[qubit\_list], \[clbit\_list]).
*   **ctrl\_state** (`Union`\[`int`, `str`, `None`]) – The control state in decimal or as a bitstring (e.g. ‘111’). If specified as a bitstring the length must equal num\_ctrl\_qubits, MSB on left. If None, use 2\*\*num\_ctrl\_qubits-1.
*   **base\_gate** (`Optional`\[`Gate`]) – Gate object to be controlled.

**Raises**

*   **CircuitError** – If `num_ctrl_qubits` >= `num_qubits`.
*   **CircuitError** – ctrl\_state \< 0 or ctrl\_state > 2\*\*num\_ctrl\_qubits.

Examples:

Create a controlled standard gate and apply it to a circuit.

```python
from qiskit import QuantumCircuit, QuantumRegister
from qiskit.circuit.library.standard_gates import HGate

qr = QuantumRegister(3)
qc = QuantumCircuit(qr)
c3h_gate = HGate().control(2)
qc.append(c3h_gate, qr)
qc.draw()
```

```python
           
q0_0: ──■──
        │  
q0_1: ──■──
      ┌─┴─┐
q0_2: ┤ H ├
      └───┘
```

Create a controlled custom gate and apply it to a circuit.

```python
from qiskit import QuantumCircuit, QuantumRegister
from qiskit.circuit.library.standard_gates import HGate

qc1 = QuantumCircuit(2)
qc1.x(0)
qc1.h(1)
custom = qc1.to_gate().control(2)

qc2 = QuantumCircuit(4)
qc2.append(custom, [0, 3, 1, 2])
qc2.draw()
```

```python
                   
q_0: ──────■───────
     ┌─────┴──────┐
q_1: ┤0           ├
     │  circuit14 │
q_2: ┤1           ├
     └─────┬──────┘
q_3: ──────■───────
                   
```

<span id="undefined" />

`__init__(name, num_qubits, params, label=None, num_ctrl_qubits=1, definition=None, ctrl_state=None, base_gate=None)`

Create a new ControlledGate. In the new gate the first `num_ctrl_qubits` of the gate are the controls.

**Parameters**

*   **name** (`str`) – The name of the gate.
*   **num\_qubits** (`int`) – The number of qubits the gate acts on.
*   **params** (`List`) – A list of parameters for the gate.
*   **label** (`Optional`\[`str`]) – An optional label for the gate.
*   **num\_ctrl\_qubits** (`Optional`\[`int`]) – Number of control qubits.
*   **definition** (`Optional`\[`QuantumCircuit`]) – A list of gate rules for implementing this gate. The elements of the list are tuples of ([`Gate()`](qiskit.circuit.Gate#qiskit.circuit.Gate "qiskit.circuit.Gate"), \[qubit\_list], \[clbit\_list]).
*   **ctrl\_state** (`Union`\[`int`, `str`, `None`]) – The control state in decimal or as a bitstring (e.g. ‘111’). If specified as a bitstring the length must equal num\_ctrl\_qubits, MSB on left. If None, use 2\*\*num\_ctrl\_qubits-1.
*   **base\_gate** (`Optional`\[`Gate`]) – Gate object to be controlled.

**Raises**

*   **CircuitError** – If `num_ctrl_qubits` >= `num_qubits`.
*   **CircuitError** – ctrl\_state \< 0 or ctrl\_state > 2\*\*num\_ctrl\_qubits.

Examples:

Create a controlled standard gate and apply it to a circuit.

```python
from qiskit import QuantumCircuit, QuantumRegister
from qiskit.circuit.library.standard_gates import HGate

qr = QuantumRegister(3)
qc = QuantumCircuit(qr)
c3h_gate = HGate().control(2)
qc.append(c3h_gate, qr)
qc.draw()
```

```python
           
q1_0: ──■──
        │  
q1_1: ──■──
      ┌─┴─┐
q1_2: ┤ H ├
      └───┘
```

Create a controlled custom gate and apply it to a circuit.

```python
from qiskit import QuantumCircuit, QuantumRegister
from qiskit.circuit.library.standard_gates import HGate

qc1 = QuantumCircuit(2)
qc1.x(0)
qc1.h(1)
custom = qc1.to_gate().control(2)

qc2 = QuantumCircuit(4)
qc2.append(custom, [0, 3, 1, 2])
qc2.draw()
```

```python
                   
q_0: ──────■───────
     ┌─────┴──────┐
q_1: ┤0           ├
     │  circuit31 │
q_2: ┤1           ├
     └─────┬──────┘
q_3: ──────■───────
                   
```

## Methods

|                                                                                                                                               |                                                                          |
| --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| [`__init__`](#qiskit.circuit.ControlledGate.__init__ "qiskit.circuit.ControlledGate.__init__")(name, num\_qubits, params\[, label, …])        | Create a new ControlledGate.                                             |
| [`add_decomposition`](#qiskit.circuit.ControlledGate.add_decomposition "qiskit.circuit.ControlledGate.add_decomposition")(decomposition)      | Add a decomposition of the instruction to the SessionEquivalenceLibrary. |
| [`assemble`](#qiskit.circuit.ControlledGate.assemble "qiskit.circuit.ControlledGate.assemble")()                                              | Assemble a QasmQobjInstruction                                           |
| [`broadcast_arguments`](#qiskit.circuit.ControlledGate.broadcast_arguments "qiskit.circuit.ControlledGate.broadcast_arguments")(qargs, cargs) | Validation and handling of the arguments and its relationship.           |
| [`c_if`](#qiskit.circuit.ControlledGate.c_if "qiskit.circuit.ControlledGate.c_if")(classical, val)                                            | Add classical condition on register classical and value val.             |
| [`control`](#qiskit.circuit.ControlledGate.control "qiskit.circuit.ControlledGate.control")(\[num\_ctrl\_qubits, label, ctrl\_state])         | Return controlled version of gate.                                       |
| [`copy`](#qiskit.circuit.ControlledGate.copy "qiskit.circuit.ControlledGate.copy")(\[name])                                                   | Copy of the instruction.                                                 |
| [`inverse`](#qiskit.circuit.ControlledGate.inverse "qiskit.circuit.ControlledGate.inverse")()                                                 | Invert this gate by calling inverse on the base gate.                    |
| [`is_parameterized`](#qiskit.circuit.ControlledGate.is_parameterized "qiskit.circuit.ControlledGate.is_parameterized")()                      | Return True .IFF.                                                        |
| [`mirror`](#qiskit.circuit.ControlledGate.mirror "qiskit.circuit.ControlledGate.mirror")()                                                    | DEPRECATED: use instruction.reverse\_ops().                              |
| [`power`](#qiskit.circuit.ControlledGate.power "qiskit.circuit.ControlledGate.power")(exponent)                                               | Creates a unitary gate as gate^exponent.                                 |
| [`qasm`](#qiskit.circuit.ControlledGate.qasm "qiskit.circuit.ControlledGate.qasm")()                                                          | Return a default OpenQASM string for the instruction.                    |
| [`repeat`](#qiskit.circuit.ControlledGate.repeat "qiskit.circuit.ControlledGate.repeat")(n)                                                   | Creates an instruction with gate repeated n amount of times.             |
| [`reverse_ops`](#qiskit.circuit.ControlledGate.reverse_ops "qiskit.circuit.ControlledGate.reverse_ops")()                                     | For a composite instruction, reverse the order of sub-instructions.      |
| [`to_matrix`](#qiskit.circuit.ControlledGate.to_matrix "qiskit.circuit.ControlledGate.to_matrix")()                                           | Return a Numpy.array for the gate unitary matrix.                        |
| [`validate_parameter`](#qiskit.circuit.ControlledGate.validate_parameter "qiskit.circuit.ControlledGate.validate_parameter")(parameter)       | Gate parameters should be int, float, or ParameterExpression             |

## Attributes

|                                                                                                                     |                                                                               |
| ------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [`ctrl_state`](#qiskit.circuit.ControlledGate.ctrl_state "qiskit.circuit.ControlledGate.ctrl_state")                | Return the control state of the gate as a decimal integer.                    |
| [`decompositions`](#qiskit.circuit.ControlledGate.decompositions "qiskit.circuit.ControlledGate.decompositions")    | Get the decompositions of the instruction from the SessionEquivalenceLibrary. |
| [`definition`](#qiskit.circuit.ControlledGate.definition "qiskit.circuit.ControlledGate.definition")                | Return definition in terms of other basic gates.                              |
| [`duration`](#qiskit.circuit.ControlledGate.duration "qiskit.circuit.ControlledGate.duration")                      | Get the duration.                                                             |
| [`label`](#qiskit.circuit.ControlledGate.label "qiskit.circuit.ControlledGate.label")                               | Return gate label                                                             |
| [`num_ctrl_qubits`](#qiskit.circuit.ControlledGate.num_ctrl_qubits "qiskit.circuit.ControlledGate.num_ctrl_qubits") | Get number of control qubits.                                                 |
| [`params`](#qiskit.circuit.ControlledGate.params "qiskit.circuit.ControlledGate.params")                            | Get parameters from base\_gate.                                               |
| [`unit`](#qiskit.circuit.ControlledGate.unit "qiskit.circuit.ControlledGate.unit")                                  | Get the time unit of duration.                                                |

<span id="undefined" />

`add_decomposition(decomposition)`

Add a decomposition of the instruction to the SessionEquivalenceLibrary.

<span id="undefined" />

`assemble()`

Assemble a QasmQobjInstruction

**Return type**

`Instruction`

<span id="undefined" />

`broadcast_arguments(qargs, cargs)`

Validation and handling of the arguments and its relationship.

For example, `cx([q[0],q[1]], q[2])` means `cx(q[0], q[2]); cx(q[1], q[2])`. This method yields the arguments in the right grouping. In the given example:

```python
in: [[q[0],q[1]], q[2]],[]
outs: [q[0], q[2]], []
      [q[1], q[2]], []
```

The general broadcasting rules are:

> *   If len(qargs) == 1:
>
>     ```python
>     [q[0], q[1]] -> [q[0]],[q[1]]
>     ```
>
> *   If len(qargs) == 2:
>
>     ```python
>     [[q[0], q[1]], [r[0], r[1]]] -> [q[0], r[0]], [q[1], r[1]]
>     [[q[0]], [r[0], r[1]]]       -> [q[0], r[0]], [q[0], r[1]]
>     [[q[0], q[1]], [r[0]]]       -> [q[0], r[0]], [q[1], r[0]]
>     ```
>
> *   If len(qargs) >= 3:
>
>     ```python
>     [q[0], q[1]], [r[0], r[1]],  ...] -> [q[0], r[0], ...], [q[1], r[1], ...]
>     ```

**Parameters**

*   **qargs** (`List`) – List of quantum bit arguments.
*   **cargs** (`List`) – List of classical bit arguments.

**Return type**

`Tuple`\[`List`, `List`]

**Returns**

A tuple with single arguments.

**Raises**

**CircuitError** – If the input is not valid. For example, the number of arguments does not match the gate expectation.

<span id="undefined" />

`c_if(classical, val)`

Add classical condition on register classical and value val.

<span id="undefined" />

`control(num_ctrl_qubits=1, label=None, ctrl_state=None)`

Return controlled version of gate. See [`ControlledGate`](#qiskit.circuit.ControlledGate "qiskit.circuit.ControlledGate") for usage.

**Parameters**

*   **num\_ctrl\_qubits** (`Optional`\[`int`]) – number of controls to add to gate (default=1)
*   **label** (`Optional`\[`str`]) – optional gate label
*   **ctrl\_state** (`Union`\[`int`, `str`, `None`]) – The control state in decimal or as a bitstring (e.g. ‘111’). If None, use 2\*\*num\_ctrl\_qubits-1.

**Returns**

Controlled version of gate. This default algorithm uses num\_ctrl\_qubits-1 ancillae qubits so returns a gate of size num\_qubits + 2\*num\_ctrl\_qubits - 1.

**Return type**

[qiskit.circuit.ControlledGate](#qiskit.circuit.ControlledGate "qiskit.circuit.ControlledGate")

**Raises**

**QiskitError** – unrecognized mode or invalid ctrl\_state

<span id="undefined" />

`copy(name=None)`

Copy of the instruction.

**Parameters**

**name** (*str*) – name to be given to the copied circuit, if None then the name stays the same.

**Returns**

**a copy of the current instruction, with the name**

updated if it was provided

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

<span id="undefined" />

`property ctrl_state`

Return the control state of the gate as a decimal integer.

**Return type**

`int`

<span id="undefined" />

`property decompositions`

Get the decompositions of the instruction from the SessionEquivalenceLibrary.

<span id="undefined" />

`property definition`

Return definition in terms of other basic gates. If the gate has open controls, as determined from self.ctrl\_state, the returned definition is conjugated with X without changing the internal \_definition.

**Return type**

`List`

<span id="undefined" />

`property duration`

Get the duration.

<span id="undefined" />

`inverse()`

Invert this gate by calling inverse on the base gate.

**Return type**

`ControlledGate`

<span id="undefined" />

`is_parameterized()`

Return True .IFF. instruction is parameterized else False

<span id="undefined" />

`property label`

Return gate label

**Return type**

`str`

<span id="undefined" />

`mirror()`

DEPRECATED: use instruction.reverse\_ops().

**Returns**

**a new instruction with sub-instructions**

reversed.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

<span id="undefined" />

`property num_ctrl_qubits`

Get number of control qubits.

**Returns**

The number of control qubits for the gate.

**Return type**

int

<span id="undefined" />

`property params`

Get parameters from base\_gate.

**Returns**

List of gate parameters.

**Return type**

list

**Raises**

**CircuitError** – Controlled gate does not define a base gate

<span id="undefined" />

`power(exponent)`

Creates a unitary gate as gate^exponent.

**Parameters**

**exponent** (*float*) – Gate^exponent

**Returns**

To which to\_matrix is self.to\_matrix^exponent.

**Return type**

[qiskit.extensions.UnitaryGate](qiskit.extensions.UnitaryGate#qiskit.extensions.UnitaryGate "qiskit.extensions.UnitaryGate")

**Raises**

**CircuitError** – If Gate is not unitary

<span id="undefined" />

`qasm()`

Return a default OpenQASM string for the instruction.

Derived instructions may override this to print in a different format (e.g. measure q\[0] -> c\[0];).

<span id="undefined" />

`repeat(n)`

Creates an instruction with gate repeated n amount of times.

**Parameters**

**n** (*int*) – Number of times to repeat the instruction

**Returns**

Containing the definition.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

**Raises**

**CircuitError** – If n \< 1.

<span id="undefined" />

`reverse_ops()`

For a composite instruction, reverse the order of sub-instructions.

This is done by recursively reversing all sub-instructions. It does not invert any gate.

**Returns**

**a new instruction with**

sub-instructions reversed.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

<span id="undefined" />

`to_matrix()`

Return a Numpy.array for the gate unitary matrix.

**Raises**

**CircuitError** – If a Gate subclass does not implement this method an exception will be raised when this base class method is called.

**Return type**

`ndarray`

<span id="undefined" />

`property unit`

Get the time unit of duration.

<span id="undefined" />

`validate_parameter(parameter)`

Gate parameters should be int, float, or ParameterExpression