# qiskit.aqua.operators.primitive\_ops.MatrixOp

<span id="undefined" />

`MatrixOp(primitive, coeff=1.0)`

Class for Operators represented by matrices, backed by Terra’s `Operator` module.

**Parameters**

*   **primitive** (`Union`\[`list`, `ndarray`, `spmatrix`, `Operator`]) – The matrix-like object which defines the behavior of the underlying function.
*   **coeff** (`Union`\[`int`, `float`, `complex`, `ParameterExpression`]) – A coefficient multiplying the primitive

**Raises**

*   **TypeError** – invalid parameters.
*   **ValueError** – invalid parameters.

<span id="undefined" />

`__init__(primitive, coeff=1.0)`

**Parameters**

*   **primitive** (`Union`\[`list`, `ndarray`, `spmatrix`, `Operator`]) – The matrix-like object which defines the behavior of the underlying function.
*   **coeff** (`Union`\[`int`, `float`, `complex`, `ParameterExpression`]) – A coefficient multiplying the primitive

**Raises**

*   **TypeError** – invalid parameters.
*   **ValueError** – invalid parameters.

## Methods

|                                                                                                                                                                      |                                                                                                                                                                               |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`__init__`](#qiskit.aqua.operators.primitive_ops.MatrixOp.__init__ "qiskit.aqua.operators.primitive_ops.MatrixOp.__init__")(primitive\[, coeff])                    | **type primitive**`Union`\[`list`, `ndarray`, `spmatrix`, `Operator`]                                                                                                         |
| [`add`](#qiskit.aqua.operators.primitive_ops.MatrixOp.add "qiskit.aqua.operators.primitive_ops.MatrixOp.add")(other)                                                 | Return Operator addition of self and other, overloaded by `+`.                                                                                                                |
| [`adjoint`](#qiskit.aqua.operators.primitive_ops.MatrixOp.adjoint "qiskit.aqua.operators.primitive_ops.MatrixOp.adjoint")()                                          | Return a new Operator equal to the Operator’s adjoint (conjugate transpose), overloaded by `~`.                                                                               |
| [`assign_parameters`](#qiskit.aqua.operators.primitive_ops.MatrixOp.assign_parameters "qiskit.aqua.operators.primitive_ops.MatrixOp.assign_parameters")(param\_dict) | Binds scalar values to any Terra `Parameters` in the coefficients or primitives of the Operator, or substitutes one `Parameter` for another.                                  |
| [`bind_parameters`](#qiskit.aqua.operators.primitive_ops.MatrixOp.bind_parameters "qiskit.aqua.operators.primitive_ops.MatrixOp.bind_parameters")(param\_dict)       | Same as assign\_parameters, but maintained for consistency with QuantumCircuit in Terra (which has both assign\_parameters and bind\_parameters).                             |
| [`compose`](#qiskit.aqua.operators.primitive_ops.MatrixOp.compose "qiskit.aqua.operators.primitive_ops.MatrixOp.compose")(other\[, permutation, front])              | Return Operator Composition between self and other (linear algebra-style: A\@B(x) = A(B(x))), overloaded by `@`.                                                              |
| [`equals`](#qiskit.aqua.operators.primitive_ops.MatrixOp.equals "qiskit.aqua.operators.primitive_ops.MatrixOp.equals")(other)                                        | Evaluate Equality between Operators, overloaded by `==`.                                                                                                                      |
| [`eval`](#qiskit.aqua.operators.primitive_ops.MatrixOp.eval "qiskit.aqua.operators.primitive_ops.MatrixOp.eval")(\[front])                                           | Evaluate the Operator’s underlying function, either on a binary string or another Operator.                                                                                   |
| [`exp_i`](#qiskit.aqua.operators.primitive_ops.MatrixOp.exp_i "qiskit.aqua.operators.primitive_ops.MatrixOp.exp_i")()                                                | Return a `CircuitOp` equivalent to e^-iH for this operator H                                                                                                                  |
| [`log_i`](#qiskit.aqua.operators.primitive_ops.MatrixOp.log_i "qiskit.aqua.operators.primitive_ops.MatrixOp.log_i")(\[massive])                                      | Return a `MatrixOp` equivalent to log(H)/-i for this operator H.                                                                                                              |
| [`mul`](#qiskit.aqua.operators.primitive_ops.MatrixOp.mul "qiskit.aqua.operators.primitive_ops.MatrixOp.mul")(scalar)                                                | Returns the scalar multiplication of the Operator, overloaded by `*`, including support for Terra’s `Parameters`, which can be bound to values later (via `bind_parameters`). |
| [`neg`](#qiskit.aqua.operators.primitive_ops.MatrixOp.neg "qiskit.aqua.operators.primitive_ops.MatrixOp.neg")()                                                      | Return the Operator’s negation, effectively just multiplying by -1.0, overloaded by `-`.                                                                                      |
| [`permute`](#qiskit.aqua.operators.primitive_ops.MatrixOp.permute "qiskit.aqua.operators.primitive_ops.MatrixOp.permute")(\[permutation])                            | Creates a new MatrixOp that acts on the permuted qubits.                                                                                                                      |
| [`power`](#qiskit.aqua.operators.primitive_ops.MatrixOp.power "qiskit.aqua.operators.primitive_ops.MatrixOp.power")(exponent)                                        | Return Operator composed with self multiple times, overloaded by `**`.                                                                                                        |
| [`primitive_strings`](#qiskit.aqua.operators.primitive_ops.MatrixOp.primitive_strings "qiskit.aqua.operators.primitive_ops.MatrixOp.primitive_strings")()            | Return a set of strings describing the primitives contained in the Operator.                                                                                                  |
| [`reduce`](#qiskit.aqua.operators.primitive_ops.MatrixOp.reduce "qiskit.aqua.operators.primitive_ops.MatrixOp.reduce")()                                             | Try collapsing the Operator structure, usually after some type of conversion, e.g.                                                                                            |
| [`tensor`](#qiskit.aqua.operators.primitive_ops.MatrixOp.tensor "qiskit.aqua.operators.primitive_ops.MatrixOp.tensor")(other)                                        | Return tensor product between self and other, overloaded by `^`.                                                                                                              |
| [`tensorpower`](#qiskit.aqua.operators.primitive_ops.MatrixOp.tensorpower "qiskit.aqua.operators.primitive_ops.MatrixOp.tensorpower")(other)                         | Return tensor product with self multiple times, overloaded by `^`.                                                                                                            |
| [`to_circuit`](#qiskit.aqua.operators.primitive_ops.MatrixOp.to_circuit "qiskit.aqua.operators.primitive_ops.MatrixOp.to_circuit")()                                 | Returns a `QuantumCircuit` equivalent to this Operator.                                                                                                                       |
| [`to_circuit_op`](#qiskit.aqua.operators.primitive_ops.MatrixOp.to_circuit_op "qiskit.aqua.operators.primitive_ops.MatrixOp.to_circuit_op")()                        | Returns a `CircuitOp` equivalent to this Operator.                                                                                                                            |
| [`to_instruction`](#qiskit.aqua.operators.primitive_ops.MatrixOp.to_instruction "qiskit.aqua.operators.primitive_ops.MatrixOp.to_instruction")()                     | Returns an `Instruction` equivalent to this Operator.                                                                                                                         |
| [`to_legacy_op`](#qiskit.aqua.operators.primitive_ops.MatrixOp.to_legacy_op "qiskit.aqua.operators.primitive_ops.MatrixOp.to_legacy_op")(\[massive])                 | Attempt to return the Legacy Operator representation of the Operator.                                                                                                         |
| [`to_matrix`](#qiskit.aqua.operators.primitive_ops.MatrixOp.to_matrix "qiskit.aqua.operators.primitive_ops.MatrixOp.to_matrix")(\[massive])                          | Return NumPy representation of the Operator.                                                                                                                                  |
| [`to_matrix_op`](#qiskit.aqua.operators.primitive_ops.MatrixOp.to_matrix_op "qiskit.aqua.operators.primitive_ops.MatrixOp.to_matrix_op")(\[massive])                 | Returns a `MatrixOp` equivalent to this Operator.                                                                                                                             |
| [`to_pauli_op`](#qiskit.aqua.operators.primitive_ops.MatrixOp.to_pauli_op "qiskit.aqua.operators.primitive_ops.MatrixOp.to_pauli_op")(\[massive])                    | Returns a sum of `PauliOp` s equivalent to this Operator.                                                                                                                     |

## Attributes

|                                                                                                                                    |                                                                 |
| ---------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| `ENABLE_DEPRECATION`                                                                                                               |                                                                 |
| `INDENTATION`                                                                                                                      |                                                                 |
| [`coeff`](#qiskit.aqua.operators.primitive_ops.MatrixOp.coeff "qiskit.aqua.operators.primitive_ops.MatrixOp.coeff")                | The scalar coefficient multiplying the Operator.                |
| [`num_qubits`](#qiskit.aqua.operators.primitive_ops.MatrixOp.num_qubits "qiskit.aqua.operators.primitive_ops.MatrixOp.num_qubits") | The number of qubits over which the Operator is defined.        |
| [`parameters`](#qiskit.aqua.operators.primitive_ops.MatrixOp.parameters "qiskit.aqua.operators.primitive_ops.MatrixOp.parameters") | Return a set of Parameter objects contained in the Operator.    |
| [`primitive`](#qiskit.aqua.operators.primitive_ops.MatrixOp.primitive "qiskit.aqua.operators.primitive_ops.MatrixOp.primitive")    | The primitive defining the underlying function of the Operator. |

<span id="undefined" />

`add(other)`

Return Operator addition of self and other, overloaded by `+`.

**Parameters**

**other** (`OperatorBase`) – An `OperatorBase` with the same number of qubits as self, and in the same ‘Operator’, ‘State function’, or ‘Measurement’ category as self (i.e. the same type of underlying function).

**Return type**

`OperatorBase`

**Returns**

An `OperatorBase` equivalent to the sum of self and other.

<span id="undefined" />

`adjoint()`

Return a new Operator equal to the Operator’s adjoint (conjugate transpose), overloaded by `~`. For StateFns, this also turns the StateFn into a measurement.

**Return type**

`OperatorBase`

**Returns**

An `OperatorBase` equivalent to the adjoint of self.

<span id="undefined" />

`assign_parameters(param_dict)`

Binds scalar values to any Terra `Parameters` in the coefficients or primitives of the Operator, or substitutes one `Parameter` for another. This method differs from Terra’s `assign_parameters` in that it also supports lists of values to assign for a give `Parameter`, in which case self will be copied for each parameterization in the binding list(s), and all the copies will be returned in an `OpList`. If lists of parameterizations are used, every `Parameter` in the param\_dict must have the same length list of parameterizations.

**Parameters**

**param\_dict** (`dict`) – The dictionary of `Parameters` to replace, and values or lists of values by which to replace them.

**Return type**

`OperatorBase`

**Returns**

The `OperatorBase` with the `Parameters` in self replaced by the values or `Parameters` in param\_dict. If param\_dict contains parameterization lists, this `OperatorBase` is an `OpList`.

<span id="undefined" />

`bind_parameters(param_dict)`

Same as assign\_parameters, but maintained for consistency with QuantumCircuit in Terra (which has both assign\_parameters and bind\_parameters).

**Return type**

`OperatorBase`

<span id="undefined" />

`property coeff`

The scalar coefficient multiplying the Operator.

**Return type**

`Union`\[`int`, `float`, `complex`, `ParameterExpression`]

**Returns**

The coefficient.

<span id="undefined" />

`compose(other, permutation=None, front=False)`

Return Operator Composition between self and other (linear algebra-style: A\@B(x) = A(B(x))), overloaded by `@`.

Note: You must be conscious of Quantum Circuit vs. Linear Algebra ordering conventions. Meaning, X.compose(Y) produces an X∘Y on qubit 0, but would produce a QuantumCircuit which looks like

> -\[Y]-\[X]-

Because Terra prints circuits with the initial state at the left side of the circuit.

**Parameters**

*   **other** (`OperatorBase`) – The `OperatorBase` with which to compose self.
*   **permutation** (`Optional`\[`List`\[`int`]]) – `List[int]` which defines permutation on other operator.
*   **front** (`bool`) – If front==True, return `other.compose(self)`.

**Return type**

`OperatorBase`

**Returns**

An `OperatorBase` equivalent to the function composition of self and other.

<span id="undefined" />

`equals(other)`

Evaluate Equality between Operators, overloaded by `==`. Only returns True if self and other are of the same representation (e.g. a DictStateFn and CircuitStateFn will never be equal, even if their vector representations are equal), their underlying primitives are equal (this means for ListOps, OperatorStateFns, or EvolvedOps the equality is evaluated recursively downwards), and their coefficients are equal.

**Parameters**

**other** (`OperatorBase`) – The `OperatorBase` to compare to self.

**Return type**

`bool`

**Returns**

A bool equal to the equality of self and other.

<span id="undefined" />

`eval(front=None)`

Evaluate the Operator’s underlying function, either on a binary string or another Operator. A square binary Operator can be defined as a function taking a binary function to another binary function. This method returns the value of that function for a given StateFn or binary string. For example, `op.eval('0110').eval('1110')` can be seen as querying the Operator’s matrix representation by row 6 and column 14, and will return the complex value at those “indices.” Similarly for a StateFn, `op.eval('1011')` will return the complex value at row 11 of the vector representation of the StateFn, as all StateFns are defined to be evaluated from Zero implicitly (i.e. it is as if `.eval('0000')` is already called implicitly to always “indexing” from column 0).

If `front` is None, the matrix-representation of the operator is returned.

**Parameters**

**front** (`Union`\[`str`, `Dict`\[`str`, `complex`], `ndarray`, `OperatorBase`, `None`]) – The bitstring, dict of bitstrings (with values being coefficients), or StateFn to evaluated by the Operator’s underlying function, or None.

**Return type**

`Union`\[`OperatorBase`, `float`, `complex`]

**Returns**

The output of the Operator’s evaluation function. If self is a `StateFn`, the result is a float or complex. If self is an Operator (`PrimitiveOp, ComposedOp, SummedOp, EvolvedOp,` etc.), the result is a StateFn. If `front` is None, the matrix-representation of the operator is returned, which is a `MatrixOp` for the operators and a `VectorStateFn` for state-functions. If either self or front contain proper `ListOps` (not ListOp subclasses), the result is an n-dimensional list of complex or StateFn results, resulting from the recursive evaluation by each OperatorBase in the ListOps.

<span id="undefined" />

`exp_i()`

Return a `CircuitOp` equivalent to e^-iH for this operator H

**Return type**

`OperatorBase`

<span id="undefined" />

`log_i(massive=False)`

Return a `MatrixOp` equivalent to log(H)/-i for this operator H. This function is the effective inverse of exp\_i, equivalent to finding the Hermitian Operator which produces self when exponentiated.

**Return type**

`OperatorBase`

<span id="undefined" />

`mul(scalar)`

Returns the scalar multiplication of the Operator, overloaded by `*`, including support for Terra’s `Parameters`, which can be bound to values later (via `bind_parameters`).

**Parameters**

**scalar** (`Union`\[`int`, `float`, `complex`, `ParameterExpression`]) – The real or complex scalar by which to multiply the Operator, or the `ParameterExpression` to serve as a placeholder for a scalar factor.

**Return type**

`OperatorBase`

**Returns**

An `OperatorBase` equivalent to product of self and scalar.

<span id="undefined" />

`neg()`

Return the Operator’s negation, effectively just multiplying by -1.0, overloaded by `-`.

**Return type**

`OperatorBase`

**Returns**

An `OperatorBase` equivalent to the negation of self.

<span id="undefined" />

`property num_qubits`

The number of qubits over which the Operator is defined. If `op.num_qubits == 5`, then `op.eval('1' * 5)` will be valid, but `op.eval('11')` will not.

**Return type**

`int`

**Returns**

The number of qubits accepted by the Operator’s underlying function.

<span id="undefined" />

`property parameters`

Return a set of Parameter objects contained in the Operator.

<span id="undefined" />

`permute(permutation=None)`

Creates a new MatrixOp that acts on the permuted qubits.

**Parameters**

**permutation** (`Optional`\[`List`\[`int`]]) – A list defining where each qubit should be permuted. The qubit at index j should be permuted to position permutation\[j].

**Return type**

`MatrixOp`

**Returns**

A new MatrixOp representing the permuted operator.

**Raises**

[**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if indices do not define a new index for each qubit.

<span id="undefined" />

`power(exponent)`

Return Operator composed with self multiple times, overloaded by `**`.

**Parameters**

**exponent** (`int`) – The int number of times to compose self with itself.

**Return type**

`OperatorBase`

**Returns**

An `OperatorBase` equivalent to self composed with itself exponent times.

<span id="undefined" />

`property primitive`

The primitive defining the underlying function of the Operator.

**Return type**

`Union`\[`Instruction`, `QuantumCircuit`, `List`, `ndarray`, `spmatrix`, `Operator`, `Pauli`]

**Returns**

The primitive object.

<span id="undefined" />

`primitive_strings()`

Return a set of strings describing the primitives contained in the Operator. For example, `{'QuantumCircuit', 'Pauli'}`. For hierarchical Operators, such as `ListOps`, this can help illuminate the primitives represented in the various recursive levels, and therefore which conversions can be applied.

**Return type**

`Set`\[`str`]

**Returns**

A set of strings describing the primitives contained within the Operator.

<span id="undefined" />

`reduce()`

Try collapsing the Operator structure, usually after some type of conversion, e.g. trying to add Operators in a SummedOp or delete needless IGates in a CircuitOp. If no reduction is available, just returns self.

**Return type**

`OperatorBase`

**Returns**

The reduced `OperatorBase`.

<span id="undefined" />

`tensor(other)`

Return tensor product between self and other, overloaded by `^`. Note: You must be conscious of Qiskit’s big-endian bit printing convention. Meaning, X.tensor(Y) produces an X on qubit 0 and an Y on qubit 1, or X⨂Y, but would produce a QuantumCircuit which looks like

> -\[Y]- -\[X]-

Because Terra prints circuits and results with qubit 0 at the end of the string or circuit.

**Parameters**

**other** (`OperatorBase`) – The `OperatorBase` to tensor product with self.

**Return type**

`OperatorBase`

**Returns**

An `OperatorBase` equivalent to the tensor product of self and other.

<span id="undefined" />

`tensorpower(other)`

Return tensor product with self multiple times, overloaded by `^`.

**Parameters**

**other** (`int`) – The int number of times to tensor product self with itself via `tensorpower`.

**Return type**

`Union`\[`OperatorBase`, `int`]

**Returns**

An `OperatorBase` equivalent to the tensorpower of self by other.

<span id="undefined" />

`to_circuit()`

Returns a `QuantumCircuit` equivalent to this Operator.

**Return type**

`QuantumCircuit`

<span id="undefined" />

`to_circuit_op()`

Returns a `CircuitOp` equivalent to this Operator.

**Return type**

`OperatorBase`

<span id="undefined" />

`to_instruction()`

Returns an `Instruction` equivalent to this Operator.

**Return type**

`Instruction`

<span id="undefined" />

`to_legacy_op(massive=False)`

Attempt to return the Legacy Operator representation of the Operator. If self is a `SummedOp` of `PauliOps`, will attempt to convert to `WeightedPauliOperator`, and otherwise will simply convert to `MatrixOp` and then to `MatrixOperator`. The Legacy Operators cannot represent `StateFns` or proper `ListOps` (meaning not one of the `ListOp` subclasses), so an error will be thrown if this method is called on such an Operator. Also, Legacy Operators cannot represent unbound Parameter coeffs, so an error will be thrown if any are present in self.

Warn if more than 16 qubits to force having to set `massive=True` if such a large vector is desired.

**Return type**

`MatrixOperator`

**Returns**

The `LegacyBaseOperator` representing this Operator.

**Raises**

**TypeError** – self is an Operator which cannot be represented by a `LegacyBaseOperator`, such as `StateFn`, proper (non-subclass) `ListOp`, or an Operator with an unbound coeff Parameter.

<span id="undefined" />

`to_matrix(massive=False)`

Return NumPy representation of the Operator. Represents the evaluation of the Operator’s underlying function on every combination of basis binary strings. Warn if more than 16 qubits to force having to set `massive=True` if such a large vector is desired.

**Return type**

`ndarray`

**Returns**

The NumPy `ndarray` equivalent to this Operator.

<span id="undefined" />

`to_matrix_op(massive=False)`

Returns a `MatrixOp` equivalent to this Operator.

**Return type**

`OperatorBase`

<span id="undefined" />

`to_pauli_op(massive=False)`

Returns a sum of `PauliOp` s equivalent to this Operator.

**Return type**

`OperatorBase`