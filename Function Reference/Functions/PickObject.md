# PickObject

## Description
Function PickObject returns a handle to an object in the document. The function receives a coordinate location, specified by parameter p, and checks this location for the presence of an object. If an object exists at the location, the function returns a handle to the object.

```pascal
FUNCTION PickObject(pX,pY : REAL): HANDLE;
```

```python
def vs.PickObject(p):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinate location to test for object.|

## Remarks
Only picks objects on the active class &amp; layer, or on other classes/layers if the class/layer options are set to Show/Snap/Modify (respectively). Essentially, it will only pick an object that you could have picked manually with the Selection Tool. Same goes for the GetPickObjectInfo function.

PickObject & HCenter (when used together?) are less likely to produce incorrect results if you zoom in first.

## Examples
[IsolateLayer](examples/IsolateLayer.md)

## See Also
VS Functions:
[GetPickObjectInfo](GetPickObjectInfo.md) 
| [ForEachObjectAtPoint](ForEachObjectAtPoint.md)

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
