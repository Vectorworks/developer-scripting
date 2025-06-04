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

## See Also
VS Functions:
[AddToPIOStyleEdit](AddToPIOStyleEdit.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
