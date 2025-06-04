# CC_GetCircuitDest

## Description
Gets handles for the destination device and socket of a circuit.

```pascal
PROCEDURE CC_GetCircuitDest(
				hCircuit     : HANDLE;
				VAR hDevice  : HANDLE;
				VAR hDevSkt  : HANDLE;
				VAR hAdapter : HANDLE;
				VAR hSocket  : HANDLE);
```

```python
def vs.CC_GetCircuitDest(hCircuit):
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
