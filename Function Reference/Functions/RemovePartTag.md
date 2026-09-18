# RemovePartTag

## Description
Remove the part tag and all part information from the specified sub-object.

```pascal
FUNCTION RemovePartTag(objectHandle : HANDLE): BOOLEAN;
```

```python
def vs.RemovePartTag(objectHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The sub-object handle.|

## Examples
```pascal
resultOK := RemovePartTag(objectHandle);
```
```python
import vs

# Remove the part tag and all part information from the specified sub-object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.RemovePartTag(objectHandle)
if ok:
    vs.Message('RemovePartTag succeeded')
else:
    vs.Message('RemovePartTag failed')
```

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
