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
==== VectorScript ====
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
==== Python ====
```python
hObject = vs.FSActLayer()
ok = vs.IFC_ClearAllPsets(hObject)
```

## Version
Availability: from Vectorworks 2011

## Category
* [IFC](../Categories/IFC.md)
