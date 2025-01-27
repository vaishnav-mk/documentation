---
title: play
description: API reference for qiskit.pulse.builder.play
in_page_toc_min_heading_level: 1
python_api_type: function
python_api_name: qiskit.pulse.builder.play
---

<span id="qiskit-pulse-builder-play" />

# qiskit.pulse.builder.play

<span id="qiskit.pulse.builder.play" />

`play(pulse, channel, name=None)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/pulse/builder.py "view source code")

Play a `pulse` on a `channel`.

Examples:

```python
from qiskit import pulse

d0 = pulse.DriveChannel(0)

with pulse.build() as pulse_prog:
    pulse.play(pulse.Constant(10, 1.0), d0)
```

**Parameters**

*   **pulse** (*Pulse |* [*ndarray*](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.html#numpy.ndarray "(in NumPy v1.25)")) – Pulse to play.
*   **channel** (*PulseChannel*) – Channel to play pulse on.
*   **name** (*str | None*) – Name of the pulse.

