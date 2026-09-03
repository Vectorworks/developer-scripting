# SM_FromShape

## Description
Creates a Structural Member from the given shape. The shape must be polygon, polyline or 3D polygon. Returns the handle of the created Structural Member.

```pascal
FUNCTION SM_FromShape(hObj : HANDLE) : HANDLE;
```

```python

def vs.SM_FromShape(hObj):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE||

## Examples
```pascal
BEGIN
	gPluginObjH := SM_FromShape(h);
END;	{of MakeStructuralMember}
```
```python
import vs

# Creates a Structural Member from the given shape.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.SM_FromShape(hObj)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2024

## Category
* [StructuralMember](../Categories/StructuralMember.md)
