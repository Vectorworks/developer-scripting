# SetWallInsertLocOff

## Description
Sets the wall insert location offset of a symbol definition, plug-in object style, or plug-in object.

```pascal
FUNCTION SetWallInsertLocOff(
				hObject              : HANDLE;
				insertLocationOffset : REAL (Coordinate)): BOOLEAN;
```

```python
def vs.SetWallInsertLocOff(hObject, insertLocationOffset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|insertLocationOffset|REAL (Coordinate)|The wall insert location offset.|

## See Also
VS Functions:
[GetWallInsertLocOff](GetWallInsertLocOff.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
