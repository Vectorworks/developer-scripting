# GetCustomObjectWallHoleGroup

## Description
Access the handle to wall hole group. This group contains geometry that defines the opening that will be cut into the wall for this parametric object.

See [[VS:Parametric Custom Opening in Wall]] for more info.

```pascal
FUNCTION GetCustomObjectWallHoleGroup(objectHand : HANDLE): HANDLE;
```

```python
def vs.GetCustomObjectWallHoleGroup(objectHand):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to custom object.|

## Examples
```pascal
resultH := GetCustomObjectWallHoleGroup(objectHand);
```
```python
import vs

# Access the handle to wall hole group.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetCustomObjectWallHoleGroup(objectHand)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks14.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
