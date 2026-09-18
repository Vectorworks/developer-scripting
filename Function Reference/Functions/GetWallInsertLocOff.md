# GetWallInsertLocOff

## Description
Gets the wall insert location offset of a symbol definition, plug-in object style, or plug-in object.

```pascal
FUNCTION GetWallInsertLocOff(hObject : HANDLE): REAL;
```

```python
def vs.GetWallInsertLocOff(hObject):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|

## Examples
```pascal
resultVal := GetWallInsertLocOff(hObject);
```
```python
import vs

# Gets the wall insert location offset of a symbol definition, plug-in object
# style, or plug-in object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetWallInsertLocOff(hObject)
vs.Message('GetWallInsertLocOff returned: ' + str(value))
```

## See Also
VS Functions:
[SetWallInsertLocOff](SetWallInsertLocOff.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
