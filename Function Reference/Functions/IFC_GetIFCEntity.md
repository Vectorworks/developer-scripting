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

```pascal
resultOK := IFC_GetIFCEntity(hObject, 'Example');
```
```python
import vs

# This function gets IFC entity name for the given object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, outStrName = vs.IFC_GetIFCEntity(hObject)
vs.Message('IFC_GetIFCEntity returned: ' + str((ok, outStrName)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
