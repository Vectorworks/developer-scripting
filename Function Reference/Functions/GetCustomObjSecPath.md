# GetCustomObjSecPath

## Description
Returns a handle to the second path polygon of a path custom object.

```pascal
FUNCTION GetCustomObjSecPath(objectHand : HANDLE): HANDLE;
```

```python
def vs.GetCustomObjSecPath(objectHand):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to object.|

## Examples
```pascal
resultH := GetCustomObjSecPath(objectHand);
```
```python
import vs

# Returns a handle to the second path polygon of a path custom object.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetCustomObjSecPath(objectHand)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[GetCustomObjectPath](GetCustomObjectPath.md)

## Version
Availability: from Vectorworks 2023.3

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
