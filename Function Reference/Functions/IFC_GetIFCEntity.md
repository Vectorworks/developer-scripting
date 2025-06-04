# IFC_GetIFCEntity

## Description
This function gets IFC entity name for the given object.

```pascal
FUNCTION IFC_GetIFCEntity(
				hObject        : HANDLE;
				VAR outStrName : STRING): BOOLEAN;
```

```python
def vs.IFC_GetIFCEntity(hObject):
    return (BOOLEAN, outStrName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|
|outStrName|STRING|Name of the IFC entity|

## Examples
Try to get the IFC entity name for the given object:
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	strName : STRING;
	hObject : HANDLE;
	ok : BOOLEAN;
begin
	hObject := FSActLayer;
	ok := IFC_GetIFCEntity(hObject, strName);
	AlrtDialog(strName);
end;

Run(Test);
```
#### Python ####
```python
hObject = vs.FSActLayer()
ok, strName = vs.IFC_GetIFCEntity(hObject)
vs.AlrtDialog(strName)
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
