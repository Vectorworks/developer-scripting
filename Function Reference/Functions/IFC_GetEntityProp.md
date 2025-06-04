# IFC_GetEntityProp

## Description
Gets the value and type of a selected property from the IFC entity.

```pascal
FUNCTION IFC_GetEntityProp(
				hObject             : HANDLE;
				inStrPropName       : STRING;
				VAR outStrPropValue : STRING;
				VAR outTypeSelect   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetEntityProp(hObject, inStrPropName):
    return (BOOLEAN, outStrPropValue, outTypeSelect)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|
|inStrPropName|STRING|Name of the property|
|outStrPropValue|STRING|Value of the property|
|outTypeSelect|INTEGER|Type of the property|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	strPropValue: STRING;
	hExtrude : HANDLE;
	iType : INTEGER;
	ok : BOOLEAN;
BEGIN
	hExtrude:= FSActLayer;
	ok := IFC_GetEntityProp(hExtrude, 'PredefinedType', strPropValue, iType);
	AlrtDialog(Concat(strPropValue, ' ,  ',  iType));
END;

RUN(Test);
```
==== Python ====
```python
hExtrude = vs.FSActLayer()
ok, strPropValue, iType = vs.IFC_GetEntityProp(hExtrude, 'PredefinedType')
vs.AlrtDialog(strPropValue + ' ,  ' + str(iType))
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
