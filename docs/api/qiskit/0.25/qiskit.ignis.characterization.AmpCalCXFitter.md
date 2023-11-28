# qiskit.ignis.characterization.AmpCalCXFitter

<span id="undefined" />

`AmpCalCXFitter(backend_result, xdata, qubits, fit_p0, fit_bounds)`

Amplitude error fitter

See BaseFitter \_\_init\_\_

<span id="undefined" />

`__init__(backend_result, xdata, qubits, fit_p0, fit_bounds)`

See BaseFitter \_\_init\_\_

## Methods

|                                                                                                                                                                 |                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| [`__init__`](#qiskit.ignis.characterization.AmpCalCXFitter.__init__ "qiskit.ignis.characterization.AmpCalCXFitter.__init__")(backend\_result, xdata, qubits, …) | See BaseFitter \_\_init\_\_                             |
| [`add_data`](#qiskit.ignis.characterization.AmpCalCXFitter.add_data "qiskit.ignis.characterization.AmpCalCXFitter.add_data")(results\[, recalc, refit])         | Add new execution results to previous execution results |
| [`angle_err`](#qiskit.ignis.characterization.AmpCalCXFitter.angle_err "qiskit.ignis.characterization.AmpCalCXFitter.angle_err")(\[qind])                        | Return the gate angle error                             |
| [`fit_data`](#qiskit.ignis.characterization.AmpCalCXFitter.fit_data "qiskit.ignis.characterization.AmpCalCXFitter.fit_data")(\[qid, p0, bounds, series])        | Fit the curve.                                          |
| [`plot`](#qiskit.ignis.characterization.AmpCalCXFitter.plot "qiskit.ignis.characterization.AmpCalCXFitter.plot")(qind\[, series, ax, show\_plot])               | Plot err data.                                          |

## Attributes

|                                                                                                                                                   |                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| [`backend_result`](#qiskit.ignis.characterization.AmpCalCXFitter.backend_result "qiskit.ignis.characterization.AmpCalCXFitter.backend_result")    | Return the execution results                                                          |
| [`description`](#qiskit.ignis.characterization.AmpCalCXFitter.description "qiskit.ignis.characterization.AmpCalCXFitter.description")             | Return the fitter’s purpose, e.g.                                                     |
| [`fit_fun`](#qiskit.ignis.characterization.AmpCalCXFitter.fit_fun "qiskit.ignis.characterization.AmpCalCXFitter.fit_fun")                         | Return the function used in the fit, e.g.                                             |
| [`measured_qubits`](#qiskit.ignis.characterization.AmpCalCXFitter.measured_qubits "qiskit.ignis.characterization.AmpCalCXFitter.measured_qubits") | Return the indices of the qubits to be characterized                                  |
| [`params`](#qiskit.ignis.characterization.AmpCalCXFitter.params "qiskit.ignis.characterization.AmpCalCXFitter.params")                            | Return the fit function parameters that were calculated by curve\_fit                 |
| [`params_err`](#qiskit.ignis.characterization.AmpCalCXFitter.params_err "qiskit.ignis.characterization.AmpCalCXFitter.params_err")                | Return the error of the fit function parameters                                       |
| [`series`](#qiskit.ignis.characterization.AmpCalCXFitter.series "qiskit.ignis.characterization.AmpCalCXFitter.series")                            | Return the list of series for the data                                                |
| [`xdata`](#qiskit.ignis.characterization.AmpCalCXFitter.xdata "qiskit.ignis.characterization.AmpCalCXFitter.xdata")                               | Return the data points on the x-axis, the independenet parameter which is fit against |
| [`ydata`](#qiskit.ignis.characterization.AmpCalCXFitter.ydata "qiskit.ignis.characterization.AmpCalCXFitter.ydata")                               | Return the data points on the y-axis                                                  |

<span id="undefined" />

`add_data(results, recalc=True, refit=True)`

Add new execution results to previous execution results

**Parameters**

*   **results** (`Union`\[`Result`, `List`\[`Result`]]) – new execution results
*   **recalc** (`bool`) – whether tp recalculate the data
*   **refit** (`bool`) – whether to refit the data

<span id="undefined" />

`angle_err(qind=- 1)`

Return the gate angle error

**Parameters**

**qind** (*int*) – qubit index to return (-1 return all)

**Returns**

a list of errors

**Return type**

list

<span id="undefined" />

`property backend_result`

Return the execution results

**Return type**

`Union`\[`Result`, `List`\[`Result`]]

<span id="undefined" />

`property description`

Return the fitter’s purpose, e.g. ‘T1’

**Return type**

`str`

<span id="undefined" />

`fit_data(qid=- 1, p0=None, bounds=None, series=None)`

Fit the curve.

Compute self.\_params and self.\_params\_err

**Parameters**

*   **qid** (`int`) – qubit for fitting. If -1 fit for all the qubits
*   **p0** (`Optional`\[`List`\[`float`]]) – initial guess, equivalent to p0 in scipy.optimize
*   **bounds** (`Optional`\[`Tuple`\[`List`\[`float`], `List`\[`float`]]]) – bounds, equivalent to bounds in scipy.optimize
*   **series** (`Optional`\[`str`]) – series to fit (if None fit all)

<span id="undefined" />

`property fit_fun`

Return the function used in the fit, e.g. BaseFitter.\_exp\_fit\_fun

**Return type**

`Callable`

<span id="undefined" />

`property measured_qubits`

Return the indices of the qubits to be characterized

**Return type**

`List`\[`int`]

<span id="undefined" />

`property params`

Return the fit function parameters that were calculated by curve\_fit

**Return type**

`List`\[`float`]

<span id="undefined" />

`property params_err`

Return the error of the fit function parameters

**Return type**

`List`\[`float`]

<span id="undefined" />

`plot(qind, series='0', ax=None, show_plot=False)`

Plot err data.

**Parameters**

*   **qind** (*int*) – qubit index to plot
*   **series** (*str*) – the series to plot
*   **ax** (*Axes*) – plot axes
*   **show\_plot** (*bool*) – call plt.show()

**Returns**

The axes object

**Return type**

Axes

**Raises**

**ImportError** – if matplotlib is not installed

<span id="undefined" />

`property series`

Return the list of series for the data

**Return type**

`Optional`\[`List`\[`str`]]

<span id="undefined" />

`property xdata`

Return the data points on the x-axis, the independenet parameter which is fit against

**Return type**

`Union`\[`List`\[`float`], `array`]

<span id="undefined" />

`property ydata`

Return the data points on the y-axis

The data points are returning in the form of a list of dictionaries:

> *   **ydata\[i]\[‘mean’] is a list, where item**
>
>     no. j is the probability of success of qubit i for a circuit that lasts xdata\[j].
>
> *   **ydata\[i]\[‘std’] is a list, where ydata\[‘std’]\[j] is the**
>
>     standard deviation of the success of qubit i.

**Return type**

`List`\[`Dict`]