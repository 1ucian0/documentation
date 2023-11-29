# qiskit.providers.basicaer.BasicAerProvider

<span id="undefined" />

`BasicAerProvider`

Provider for Basic Aer backends.

<span id="undefined" />

`__init__()`

Initialize self. See help(type(self)) for accurate signature.

## Methods

|                                                                                                                                            |                                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------- |
| [`__init__`](#qiskit.providers.basicaer.BasicAerProvider.__init__ "qiskit.providers.basicaer.BasicAerProvider.__init__")()                 | Initialize self.                                            |
| [`backends`](#qiskit.providers.basicaer.BasicAerProvider.backends "qiskit.providers.basicaer.BasicAerProvider.backends")(\[name, filters]) | Return a list of backends matching the specified filtering. |
| [`get_backend`](#qiskit.providers.basicaer.BasicAerProvider.get_backend "qiskit.providers.basicaer.BasicAerProvider.get_backend")(\[name]) | Return a single backend matching the specified filtering.   |

## Attributes

|           |   |
| --------- | - |
| `version` |   |

<span id="undefined" />

`backends(name=None, filters=None, **kwargs)`

Return a list of backends matching the specified filtering.

**Parameters**

*   **name** (*str*) – name of the backend.
*   **\*\*kwargs** – dict used for filtering.

**Returns**

**a list of Backends that match the filtering**

criteria.

**Return type**

list\[[Backend](qiskit.providers.Backend#qiskit.providers.Backend "qiskit.providers.Backend")]

<span id="undefined" />

`get_backend(name=None, **kwargs)`

Return a single backend matching the specified filtering.

**Parameters**

*   **name** (*str*) – name of the backend.
*   **\*\*kwargs** – dict used for filtering.

**Returns**

a backend matching the filtering.

**Return type**

[Backend](qiskit.providers.Backend#qiskit.providers.Backend "qiskit.providers.Backend")

**Raises**

[**QiskitBackendNotFoundError**](qiskit.providers.QiskitBackendNotFoundError#qiskit.providers.QiskitBackendNotFoundError "qiskit.providers.QiskitBackendNotFoundError") – if no backend could be found or more than one backend matches the filtering criteria.