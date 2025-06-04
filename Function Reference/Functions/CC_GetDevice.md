# CC_GetDevice

## Description
Gets the parent device handle from the given socket handle.

```pascal
FUNCTION CC_GetDevice(
				hSocket       : HANDLE;
				skip adapters : BOOLEAN): HANDLE;
```

```python
def vs.CC_GetDevice(hSocket, skip adapters):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSocket|HANDLE|   |
|skip adapters|BOOLEAN|   |

## Version
Availability: from Vectorworks 2025

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
