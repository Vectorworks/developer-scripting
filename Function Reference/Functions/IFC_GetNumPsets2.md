# IFC_GetNumPsets2

## Description
Gets the number of property sets, attached to the object.

```pascal
FUNCTION IFC_GetNumPsets2(
				hObject         : HANDLE;
				bAllPsets       : BOOLEAN;
				VAR outNumPsets : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetNumPsets2(hObject, bAllPsets):
    return (BOOLEAN, outNumPsets)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object.|
|bAllPsets|BOOLEAN|Include in the list the PSets from IFC Data Mapping.|
|outNumPsets|INTEGER|Number of PSets.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	numPSets : INTEGER;
	ok : BOOLEAN;
BEGIN
	ok := IFC_GetNumPsets2(FSActLayer, TRUE, numPSets);
	AlrtDialog(Concat('The number of PSets is ', numPSets));
END;

RUN(Test);
```
#### Python ####
```python
numPSets = 0
ok, numPSets = vs.IFC_GetNumPsets2(vs.FSActLayer(), True)
vs.AlrtDialog('The number of PSets is ' + str(numPSets))
```

```pascal
resultOK := IFC_GetNumPsets2(hObject, TRUE, 1);
```
```python
import vs

# Gets the number of property sets, attached to the object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
bAllPsets = True

ok, outNumPsets = vs.IFC_GetNumPsets2(hObject, bAllPsets)
vs.Message('IFC_GetNumPsets2 returned: ' + str((ok, outNumPsets)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
