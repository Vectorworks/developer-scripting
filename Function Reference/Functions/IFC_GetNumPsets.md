# IFC_GetNumPsets

## Description
Gets the number of property sets, attached to the object

```pascal
FUNCTION IFC_GetNumPsets(
				hObject         : HANDLE;
				VAR outNumPsets : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetNumPsets(hObject):
    return (BOOLEAN, outNumPsets)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|
|outNumPsets|INTEGER|Number of PSets|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	hObject : HANDLE;
	iNum : INTEGER;
	ok : BOOLEAN;
begin
	hObject := FSActLayer;
	ok := IFC_GetNumPsets(hObject, iNum);
	AlrtDialog(Concat(iNum));
end;

Run(Test);
```
==== Python ====
```python
ok, iNum = vs.IFC_GetNumPsets(vs.FSActLayer())
vs.AlrtDialog(str(iNum))
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
