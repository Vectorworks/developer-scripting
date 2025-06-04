# IFC_GetPsetName

## Description
Gets the name of the property set at that index

```pascal
FUNCTION IFC_GetPsetName(
				hObject            : HANDLE;
				inPsetIndex        : INTEGER;
				VAR outStrPsetName : STRING): BOOLEAN;
```

```python
def vs.IFC_GetPsetName(hObject, inPsetIndex):
    return ok, outStrPsetName
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|
|inPsetIndex|INTEGER|of the property|
|outStrPsetName|STRING|Name of the pset|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	hObject : HANDLE;
	outStrPsetName : STRING;
	ok : BOOLEAN;
BEGIN
	hObject := FSActLayer;
	ok := IFC_GetPsetName(hObject, 1, outStrPsetName);
	AlrtDialog(outStrPsetName);
END;

RUN(Test);
```
#### Python ####
```python
hObject = vs.FSActLayer()
ok, outStrPsetName = vs. IFC_GetPsetName(hObject, 1)
if ok:
	vs.AlrtDialog(outStrPsetName)
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
