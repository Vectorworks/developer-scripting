# IFC_CreateObjGUID

## Description
Create a Tag record for the specified object if it doesn't have any IFC info.

```pascal
FUNCTION IFC_CreateObjGUID(hObject : HANDLE): BOOLEAN;
```

```python
def vs.IFC_CreateObjGUID(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to the object.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	hObject : HANDLE;
	ok : BOOLEAN;
BEGIN
	hObject := FSActLayer;
	ok := IFC_CreateObjGUID(hObject);
END;

RUN(Test);
```
#### Python ####
```python
hObject = vs.FSActLayer()
ok = vs.IFC_CreateObjGUID(hObject)
```

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
