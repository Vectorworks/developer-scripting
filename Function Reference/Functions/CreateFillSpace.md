# CreateFillSpace

## Description
Creates a new fillspace object and attaches it to the end of the aux list of the specified object.

```pascal
FUNCTION CreateFillSpace(owner : HANDLE): HANDLE;
```

```python
def vs.CreateFillSpace(owner):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|owner|HANDLE|Handle to the object in whose aux list the fill space will be created.|

## Examples
```pascal
resultH := CreateFillSpace(owner);
```
```python
import vs

# Creates a new fillspace object and attaches it to the end of the aux list
# of the specified object.
owner = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.CreateFillSpace(owner)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
