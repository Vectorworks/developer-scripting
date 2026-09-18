# CC_GetCircuitSource

## Description
Gets handles for the source device and socket of a circuit.

```pascal
PROCEDURE CC_GetCircuitSource(
				hCircuit     : HANDLE;
				VAR hDevice  : HANDLE;
				VAR hDevSkt  : HANDLE;
				VAR hAdapter : HANDLE;
				VAR hSocket  : HANDLE);
```

```python
def vs.CC_GetCircuitSource(hCircuit):
    return (hDevice, hDevSkt, hAdapter, hSocket)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hCircuit|HANDLE|   |
|hDevice|HANDLE|   |
|hDevSkt|HANDLE|   |
|hAdapter|HANDLE|   |
|hSocket|HANDLE|   |

## Examples
```pascal
CC_GetCircuitSource(hCircuit, hDevice, hDevSkt, hAdapter, hSocket);
```
```python
import vs

# Gets handles for the source device and socket of a circuit.
hCircuit = vs.FSActLayer()  # handle to the first selected object on the active layer

hDevice, hDevSkt, hAdapter, hSocket = vs.CC_GetCircuitSource(hCircuit)
vs.Message('CC_GetCircuitSource returned: ' + str((hDevice, hDevSkt, hAdapter, hSocket)))
```

## Version
Availability: from Vectorworks 2025

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
