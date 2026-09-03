# GetFillSpace

## Description
Returns the handle of the index-th fill space in the specified object's aux list.

```pascal
FUNCTION GetFillSpace(
				h     : HANDLE;
				index : INTEGER): HANDLE;
```

```python
def vs.GetFillSpace(h, index):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the object containing the fill space.|
|index|INTEGER|Index of the fill space to be returned.|

## Examples
```pascal
resultH := GetFillSpace(h, 1);
```
```python
import vs

# Returns the handle of the index-th fill space in the specified object's aux
# list.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

objHandle = vs.GetFillSpace(h, index)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
