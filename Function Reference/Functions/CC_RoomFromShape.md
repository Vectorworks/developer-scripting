# CC_RoomFromShape

## Description
Creates layout room from the given shape. The shape must be rectangle, rounded rectangle, polygon or polyline. Returns the handle of the created room.

```pascal
FUNCTION CC_RoomFromShape(hObj : HANDLE): HANDLE;
```

```python
def vs.CC_RoomFromShape(hObj):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|   |

## Examples
```pascal
BEGIN
	gPluginObjH := CC_RoomFromShape(h);
END;	{of MakeRoom}
{--------------------------------------------------------------------------------------------}
PROCEDURE MakeUserObject (h : HANDLE);
VAR
```
```python
import vs

# Creates layout room from the given shape.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.CC_RoomFromShape(hObj)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2022.3

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
