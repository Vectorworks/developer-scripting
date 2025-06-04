# IFC_GetPsetInfoAt

## Description
Returns the property set name, if it is attached and where from (mapping or record).

```pascal
FUNCTION IFC_GetPsetInfoAt(
				hObject            : HANDLE;
				bAllPsets          : BOOLEAN;
				index              : INTEGER;
				VAR outIfcPsetName : STRING;
				VAR outType        : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetPsetInfoAt(hObject, bAllPsets, index):
    return (BOOLEAN, outIfcPsetName, outType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object.|
|bAllPsets|BOOLEAN|Boolean that defines whether customPsets are to be checked.|
|index|INTEGER|Index that defines the pset position.|
|outIfcPsetName|STRING|Out parameter for the property set name.|
|outType|INTEGER|Returns the index that defines the state of the Pset. Possible values are: '''-2''' (pset forbidden from mapping, NOT attached in record), '''-1''' (pset forbidden from mapping, but attached in record), '''0''' (pset NOT attached), '''1''' (pset attached from record), '''2''' (pset attached from mapping).|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	hObject : HANDLE;
	ok 	: BOOLEAN;
	outName	: STRING;
	outType	: INTEGER;
	
begin
	ok := IFC_GetPsetInfoAt(hObject, true, 0, outName, outType);
END;

RUN(Test);
```
#### Python ####
```python
hObject	= vs.Handle()
ok	= False
outName	= ""
outType	= -1

ok	= vs.IFC_GetPsetInfoAt(hObject, True, 0, outName, outType)
```

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
