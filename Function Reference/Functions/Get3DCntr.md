# Get3DCntr

## Description
Procedure Get3DCntr returns the three-dimensional center point of the referenced 3D object (BoundingBox).

```pascal
PROCEDURE Get3DCntr(
				h          : HANDLE;
				VAR pX,pY  : REAL;
				VAR zValue : REAL);
```

```python
def vs.Get3DCntr(h):
    return (p, zValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|p|REAL|Returns coordinates of object center point.|
|zValue|REAL|Returns elevation of object center point.|

## Examples


## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
