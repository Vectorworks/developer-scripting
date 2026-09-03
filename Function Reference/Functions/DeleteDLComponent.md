# DeleteDLComponent

## Description
Deletes the nth component of the Double Line Preferences, where n is equal to index.

```pascal
FUNCTION DeleteDLComponent(index : INTEGER): BOOLEAN;
```

```python
def vs.DeleteDLComponent(index):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component to delete.|

## Remarks
CJG 6-27-06

## Examples
```pascal
resultOK := DeleteDLComponent(1);
```
```python
import vs

# Deletes the nth component of the Double Line Preferences, where n is equal
# to index.
index = 1

ok = vs.DeleteDLComponent(index)
if ok:
    vs.Message('DeleteDLComponent succeeded')
else:
    vs.Message('DeleteDLComponent failed')
```

## See Also
VS Functions:
[InsertNewDLComponent](InsertNewDLComponent.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
