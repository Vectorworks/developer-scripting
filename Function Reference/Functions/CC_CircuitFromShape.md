# CC_CircuitFromShape

## Description
Creates circuit from the given shape. The shape must be line, polygon or polyline.

```pascal
PROCEDURE CC_CircuitFromShape(hObj : HANDLE);
```

```python
def vs.CC_CircuitFromShape(hObj):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|   |

## Examples
```pascal
BEGIN
	gPluginObjH := CC_CircuitFromShape(h);
END;	{of MakeCircuit}
```
```python
import vs

# Creates circuit from the given shape.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.CC_CircuitFromShape(hObj)
```

## Version
Availability: from Vectorworks 2022

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
