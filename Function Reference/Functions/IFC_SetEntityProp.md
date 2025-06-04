# IFC_SetEntityProp

## Description
This function sets a value to the selected property of the IFC entity.

```pascal
FUNCTION IFC_SetEntityProp(
				hObject        : HANDLE;
				inStrPropName  : STRING;
				inStrPropValue : STRING): BOOLEAN;
```

```python
def vs.IFC_SetEntityProp(hObject, inStrPropName, inStrPropValue):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|
|inStrPropName|STRING|Name of the property|
|inStrPropValue|STRING|Value of the property|

## Examples
Assume we have an extrude, that we want to be exported as a slab. IfcSlab has a property with enumeration value (“PredefinedType”), so it’s necessary to be set:
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	hExtrude : HANDLE;
	ok : BOOLEAN;
begin
	hExtrude := FSActLayer;
	ok := IFC_SetIFCEntity(hExtrude, 'IfcSlab');
	ok := IFC_SetEntityProp(hExtrude, 'PredefinedType', 'BASESLAB');
end;

Run(Test);
```
#### Python ####
```python
hExtrude = vs.FSActLayer()
ok = vs.IFC_SetIFCEntity(hExtrude, 'IfcSlab')
ok = vs.IFC_SetEntityProp(hExtrude, 'PredefinedType', 'BASESLAB')
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
