# GetWallClosureGroup

## Description
Returns the handle to the wall closure group of an object.

```pascal
FUNCTION GetWallClosureGroup(hObject : HANDLE): HANDLE;
```

```python
def vs.GetWallClosureGroup(hObject):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to the object containing the wall closure group|

## Examples
```pascal
resultH := GetWallClosureGroup(hObject);
```
```python
import vs

# Returns the handle to the wall closure group of an object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetWallClosureGroup(hObject)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[SetWallClosureGroup](SetWallClosureGroup.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
