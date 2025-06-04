# IFC_ClearIFCInfo

## Description
Removes all IFC data

```pascal
FUNCTION IFC_ClearIFCInfo(hObject : HANDLE): BOOLEAN;
```

```python
def vs.IFC_ClearIFCInfo(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	hObject : HANDLE;
	ok : BOOLEAN;
begin
	hObject := FSActLayer;
	ok := IFC_ClearIFCInfo(hObject);
end;

RUN(Test);
```
==== Python ====
```python
hObject = vs.FSActLayer()
ok = vs.IFC_ClearIFCInfo(hObject)
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
