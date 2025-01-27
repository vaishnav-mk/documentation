---
title: deprecate_function
description: API reference for qiskit.utils.deprecate_function
in_page_toc_min_heading_level: 1
python_api_type: function
python_api_name: qiskit.utils.deprecate_function
---

<span id="qiskit-utils-deprecate-function" />

# qiskit.utils.deprecate\_function

<span id="qiskit.utils.deprecate_function" />

`deprecate_function(msg, stacklevel=2, category=<class 'DeprecationWarning'>, *, since=None)`[GitHub](https://github.com/qiskit/qiskit/tree/stable/0.24/qiskit/utils/deprecation.py "view source code")

Deprecated. Instead, use @deprecate\_func.

**Parameters**

*   **msg** (*str*) – Warning message to emit.
*   **stacklevel** (*int*) – The warning stacklevel to use, defaults to 2.
*   **category** (*Type\[Warning]*) – Usually either DeprecationWarning or PendingDeprecationWarning.
*   **since** (*str | None*) – The version the deprecation started at. Only Optional for backwards compatibility - this should always be set. If the deprecation is pending, set the version to when that started; but later, when switching from pending to deprecated, update since to the new version.

**Returns**

The decorated, deprecated callable.

**Return type**

Callable

