---
title: ControlChannel
description: API reference for qiskit.pulse.channels.ControlChannel
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.pulse.channels.ControlChannel
---

# ControlChannel

<span id="qiskit.pulse.channels.ControlChannel" />

`qiskit.pulse.channels.ControlChannel(*args, **kwargs)`

Bases: `PulseChannel`

Control channels provide supplementary control over the qubit to the drive channel. These are often associated with multi-qubit gate operations. They may not map trivially to a particular qubit index.

Channel class.

**Parameters**

**index** – Index of channel.

## Attributes

<span id="qiskit.pulse.channels.ControlChannel.index" />

### index

Return the index of this channel. The index is a label for a control signal line typically mapped trivially to a qubit index. For instance, `DriveChannel(0)` labels the signal line driving the qubit labeled with index 0.

<span id="qiskit.pulse.channels.ControlChannel.name" />

### name

Return the shorthand alias for this channel, which is based on its type and index.

<span id="qiskit.pulse.channels.ControlChannel.parameters" />

### parameters

Parameters which determine the channel index.

<span id="qiskit.pulse.channels.ControlChannel.prefix" />

### prefix

`str | None`

`= 'u'`

A shorthand string prefix for characterizing the channel type.

## Methods

### is\_parameterized

<span id="qiskit.pulse.channels.ControlChannel.is_parameterized" />

`is_parameterized()`

Return True iff the channel is parameterized.

**Return type**

[bool](https://docs.python.org/3/library/functions.html#bool "(in Python v3.11)")
