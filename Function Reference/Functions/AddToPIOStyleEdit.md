# AddToPIOStyleEdit

## Description
Adds an item to a plug-in style's default edit list. This is only used by objects that use the default edit style dialog.<BR>
<BR>
By default, only those parameters shown in the object info palette will be listed in the edit style mapping dialg. Pass the following values to add or remove an item this list.<BR>
<BR>
Values:<BR>
1 - Add to the edit style map dialog.<BR>
2 - Remove from the edit style map dialog.<BR>
<BR>
<BR>
To remove an entry from this list use RemovePIOStyleEdit.<BR>
<BR>

```pascal
FUNCTION AddToPIOStyleEdit(
				hObj        : HANDLE;
				keyName     : STRING;
				editType    : INTEGER;
				displayName : STRING): BOOLEAN;
```

```python
def vs.AddToPIOStyleEdit(hObj, keyName, editType, displayName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to a plug-in object or plug-in object style|
|keyName|STRING|Universal name of parameter or other item to add to the edit style map list|
|editType|INTEGER|1 - Add to edit list 2 - Remove from edit list|
|displayName|STRING|The display name to use in the style map dialog. If an empy string is passed the keyName will be used.|

## See Also
VS Functions:
[RemovePIOStyleEdit](RemovePIOStyleEdit.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
