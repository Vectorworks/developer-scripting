# Move3DObj

## Description
Procedure Move3DObj moves the referenced object a specified  distance from its current location. Movement distances are calculated from the 3D center of the object.

```pascal
PROCEDURE Move3DObj(
				h         : HANDLE;
				xDistance : REAL;
				yDistance : REAL;
				zDistance : REAL);
```

```python
def vs.Move3DObj(h, xDistance, yDistance, zDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|xDistance|REAL|X offset distance.|
|yDistance|REAL|Y offset distance.|
|zDistance|REAL|Z offset distance.|

## Examples
nipulate3DObjects}}

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
