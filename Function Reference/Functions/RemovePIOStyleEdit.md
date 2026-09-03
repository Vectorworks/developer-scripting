# RemovePIOStyleEdit

## Description
Removes an item from the edit style mapping list.

```pascal
FUNCTION RemovePIOStyleEdit(
				hObj    : HANDLE;
				keyName : STRING): BOOLEAN;
```

```python
def vs.RemovePIOStyleEdit(hObj, keyName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to a plug-in object or plug-in style|
|keyName|STRING|Name of item to remove from list.|

## Examples
```pascal
resultOK := RemovePIOStyleEdit(hObj, 'Example');
```
```python
import vs

# Removes an item from the edit style mapping list.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer
keyName = 'Example'

ok = vs.RemovePIOStyleEdit(hObj, keyName)
if ok:
    vs.Message('RemovePIOStyleEdit succeeded')
else:
    vs.Message('RemovePIOStyleEdit failed')
```

## See Also
VS Functions:
[AddToPIOStyleEdit](AddToPIOStyleEdit.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
