---
title: square
description: API reference for qiskit.pulse.library.square
in_page_toc_min_heading_level: 1
python_api_type: function
python_api_name: qiskit.pulse.library.square
---

# qiskit.pulse.library.square

<span id="qiskit.pulse.library.square" />

`square(duration, amp, freq=None, phase=0, name=None)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.22/qiskit/pulse/library/discrete.py "view source code")

Generates square wave [`Waveform`](qiskit.pulse.library.Waveform "qiskit.pulse.library.Waveform").

For $A=$ `amp`, $T=$ `period`, and $\phi=$ `phase`, applies the midpoint sampling strategy to generate a discrete pulse sampled from the continuous function:

$$
f(x) = A \text{sign}\left[ \sin\left(\frac{2 \pi x}{T} + 2\phi\right) \right]
$$

with the convention $\text{sign}(0) = 1$.

**Parameters**

*   **duration** (`int`) – Duration of pulse. Must be greater than zero.
*   **amp** (`complex`) – Pulse amplitude. Wave range is $[-$ `amp` $,$ `amp` $]$.
*   **freq** (`Optional`\[`float`]) – Pulse frequency, units of 1./dt. If `None` defaults to 1./duration.
*   **phase** (`float`) – Pulse phase.
*   **name** (`Optional`\[`str`]) – Name of pulse.

**Return type**

[`Waveform`](qiskit.pulse.library.Waveform "qiskit.pulse.library.waveform.Waveform")

