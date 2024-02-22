---
title: ASAPScheduleAnalysis
description: API reference for qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis
---

# ASAPScheduleAnalysis

<span id="qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis" />

`ASAPScheduleAnalysis(durations)`[GitHub](https://github.com/qiskit/qiskit-ibm-provider/tree/stable/0.9/qiskit_ibm_provider/transpiler/passes/scheduling/scheduler.py "view source code")

Dynamic circuits as-soon-as-possible (ASAP) scheduling analysis pass.

This is a scheduler designed to work for the unique scheduling constraints of the dynamic circuits backends due to the limitations imposed by hardware. This is expected to evolve over time as the dynamic circuit backends also change.

In its current form this is similar to Qiskit’s ASAP scheduler in which instructions start as early as possible.

The primary differences are that:

*   **Resets and control-flow currently trigger the end of a “quantum block”. The period between the end**

    of the block and the next is *nondeterministic* ie., we do not know when the next block will begin (as we could be evaluating a classical function of nondeterministic length) and therefore the next block starts at a *relative* t=0.

*   During a measurement it is possible to apply gates in parallel on disjoint qubits.

*   Measurements and resets on disjoint qubits happen simultaneously and are part of the same block.

Scheduler for dynamic circuit backends.

**Parameters**

**durations** ([`InstructionDurations`](https://docs.quantum.ibm.com/api/qiskit/qiskit.transpiler.InstructionDurations "(in Qiskit v0.46)")) – Durations of instructions to be used in scheduling.

## Attributes

<span id="qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis.is_analysis_pass" />

### is\_analysis\_pass

Check if the pass is an analysis pass.

If the pass is an AnalysisPass, that means that the pass can analyze the DAG and write the results of that analysis in the property set. Modifications on the DAG are not allowed by this kind of pass.

<span id="qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis.is_transformation_pass" />

### is\_transformation\_pass

Check if the pass is a transformation pass.

If the pass is a TransformationPass, that means that the pass can manipulate the DAG, but cannot modify the property set (but it can be read).

## Methods

### \_\_call\_\_

<span id="qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis.__call__" />

`__call__(circuit, property_set=None)`

Runs the pass on circuit.

**Parameters**

*   **circuit** (*QuantumCircuit*) – The dag on which the pass is run.
*   **property\_set** (*PropertySet | dict | None*) – Input/output property set. An analysis pass might change the property set in-place.

**Return type**

QuantumCircuit

**Returns**

If on transformation pass, the resulting QuantumCircuit. If analysis pass, the input circuit.

### execute

<span id="qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis.execute" />

`execute(passmanager_ir, state, callback=None)`

Execute optimization task for input Qiskit IR.

**Parameters**

*   **passmanager\_ir** (`Any`) – Qiskit IR to optimize.
*   **state** ([`PassManagerState`](https://docs.quantum.ibm.com/api/qiskit/qiskit.passmanager.PassManagerState "(in Qiskit v0.46)")) – State associated with workflow execution by the pass manager itself.
*   **callback** (`Optional`\[`Callable`]) – A callback function which is caller per execution of optimization task.

**Return type**

`tuple`\[`Any`, [`PassManagerState`](https://docs.quantum.ibm.com/api/qiskit/qiskit.passmanager.PassManagerState "(in Qiskit v0.46)")]

**Returns**

Optimized Qiskit IR and state of the workflow.

### name

<span id="qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis.name" />

`name()`

Name of the pass.

**Return type**

`str`

### run

<span id="qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis.run" />

`run(dag)`

Run the ALAPSchedule pass on dag. :type dag: [`DAGCircuit`](https://docs.quantum.ibm.com/api/qiskit/qiskit.dagcircuit.DAGCircuit "(in Qiskit v0.46)") :param dag: DAG to schedule. :type dag: DAGCircuit

**Raises**

*   **TranspilerError** – if the circuit is not mapped on physical qubits.
*   **TranspilerError** – if conditional bit is added to non-supported instruction.

**Return type**

[`DAGCircuit`](https://docs.quantum.ibm.com/api/qiskit/qiskit.dagcircuit.DAGCircuit "(in Qiskit v0.46)")

**Returns**

The scheduled DAGCircuit.

### update\_status

<span id="qiskit_ibm_provider.transpiler.passes.scheduling.ASAPScheduleAnalysis.update_status" />

`update_status(state, run_state)`

Update workflow status.

**Parameters**

*   **state** ([`PassManagerState`](https://docs.quantum.ibm.com/api/qiskit/qiskit.passmanager.PassManagerState "(in Qiskit v0.46)")) – Pass manager state to update.
*   **run\_state** (`RunState`) – Completion status of current task.

**Return type**

[`PassManagerState`](https://docs.quantum.ibm.com/api/qiskit/qiskit.passmanager.PassManagerState "(in Qiskit v0.46)")

**Returns**

Updated pass manager state.
