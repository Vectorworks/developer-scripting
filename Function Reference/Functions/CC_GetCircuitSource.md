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

## Version
Availability: from Vectorworks 2025

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
