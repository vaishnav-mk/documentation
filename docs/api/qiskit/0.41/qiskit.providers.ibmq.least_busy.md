---
title: least_busy
description: API reference for qiskit.providers.ibmq.least_busy
in_page_toc_min_heading_level: 1
python_api_type: function
python_api_name: qiskit.providers.ibmq.least_busy
---

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

# qiskit.providers.ibmq.least\_busy

<span id="qiskit.providers.ibmq.least_busy" />

`least_busy(backends, reservation_lookahead=60)`[GitHub](https://github.com/qiskit/qiskit-ibmq-provider/tree/stable/0.20/qiskit/providers/ibmq/__init__.py "view source code")

Return the least busy backend from a list.

Return the least busy available backend for those that have a `pending_jobs` in their `status`. Note that local backends may not have this attribute.

**Parameters**

*   **backends** (`List`\[[`Backend`](qiskit.providers.Backend "qiskit.providers.backend.Backend")]) – The backends to choose from.
*   **reservation\_lookahead** (`Optional`\[`int`]) – A backend is considered unavailable if it has reservations in the next `n` minutes, where `n` is the value of `reservation_lookahead`. If `None`, reservations are not taken into consideration.

**Return type**

[`Backend`](qiskit.providers.Backend "qiskit.providers.backend.Backend")

**Returns**

The backend with the fewest number of pending jobs.

**Raises**

[**IBMQError**](qiskit.providers.ibmq.IBMQError "qiskit.providers.ibmq.IBMQError") – If the backends list is empty, or if none of the backends is available, or if a backend in the list does not have the `pending_jobs` attribute in its status.

