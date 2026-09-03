# IFC_ClearAllPsets

## Description
Removes all IFC Psets.

```pascal
FUNCTION IFC_ClearAllPsets(hObject : HANDLE): BOOLEAN;
```

```python
def vs.IFC_ClearAllPsets(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	hObject : HANDLE;
	ok : BOOLEAN;
BEGIN
	hObject := FSActLayer;
	ok := IFC_ClearAllPsets(hObject);
END;

RUN(Test);
```
#### Python ####
```python
hObject = vs.FSActLayer()
ok = vs.IFC_ClearAllPsets(hObject)
```

```pascal
resultOK := IFC_ClearAllPsets(hObject);
```
```python
import vs

# Removes all IFC Psets.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IFC_ClearAllPsets(hObject)
if ok:
    vs.Message('IFC_ClearAllPsets succeeded')
else:
    vs.Message('IFC_ClearAllPsets failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [IFC](../Categories/IFC.md)
