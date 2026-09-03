# GetWallInsertLoc

## Description
Gets the wall insert location of a symbol definition, plug-in object style, or plug-in object.

```pascal
FUNCTION GetWallInsertLoc(hObject : HANDLE): INTEGER;
```

```python
def vs.GetWallInsertLoc(hObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|

## Examples
```pascal
resultN := GetWallInsertLoc(hObject);
```
```python
import vs

# Gets the wall insert location of a symbol definition, plug-in object style,
# or plug-in object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetWallInsertLoc(hObject)
vs.Message('GetWallInsertLoc returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetWallInsertLoc](SetWallInsertLoc.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
