# IFC_GetPsetProp

## Description
Gets the value and type of a selected property from a property set

```pascal
FUNCTION IFC_GetPsetProp(
				hObject             : HANDLE;
				inStrPsetName       : STRING;
				inStrPropName       : STRING;
				VAR outStrPropValue : STRING;
				VAR outTypeSelect   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetPsetProp(hObject, inStrPsetName, inStrPropName):
    return (BOOLEAN, outStrPropValue, outTypeSelect)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|
|inStrPsetName|STRING|Name of the pset|
|inStrPropName|STRING|Name of the property|
|outStrPropValue|STRING|Value of the property|
|outTypeSelect|INTEGER|Type of the property|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	hWall : HANDLE;
	outValue : STRING;
	iType : INTEGER;
	ok : BOOLEAN;
begin
	hWall := FSActLayer;
	ok := IFC_GetPsetProp(hWall, 'Pset_WallCommon', 'Reference', outValue, iType);
	AlrtDialog(Concat(outValue, ', ', iType));
END;

RUN(Test);
```
#### Python ####
```python
hWall = vs.FSActLayer()
ok, outValue, iType  = vs.IFC_GetPsetProp(hWall, 'Pset_WallCommon', 'Reference')
vs.AlrtDialog(outValue + ', ' + str(iType))
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
