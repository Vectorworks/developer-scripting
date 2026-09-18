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

## Examples
```pascal
SetWallInsertLocOff(hObject, 1.0);
```
```python
import vs

# Sets the wall insert location offset of a symbol definition, plug-in object
# style, or plug-in object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
insertLocationOffset = 0.0

ok = vs.SetWallInsertLocOff(hObject, insertLocationOffset)
if ok:
    vs.Message('SetWallInsertLocOff succeeded')
else:
    vs.Message('SetWallInsertLocOff failed')
```

## See Also
VS Functions:
[GetWallInsertLocOff](GetWallInsertLocOff.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
