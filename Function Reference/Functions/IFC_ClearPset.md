# IFC_ClearPset

## Description
Removes a Property Set from the object's attached Ifc Record.

```pascal
FUNCTION IFC_ClearPset(
				hObject       : HANDLE;
				inStrPsetName : STRING): BOOLEAN;
```

```python
def vs.IFC_ClearPset(hObject, inStrPsetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to the object.|
|inStrPsetName|STRING|The name of the Property Set.|

## Examples
Assume we want to clear a "PSet_WallCommon" from Object which has already attached Ifc Record with that Property Set:

#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	hObject : HANDLE;
	ok : BOOLEAN;
BEGIN
	hObject := FSActLayer;
	ok := IFC_ClearPset(hObject, 'PSet_WallCommon');
END;

RUN(Test);
```
#### Python ####
```python
hObject = vs.FSActLayer()
ok = vs.IFC_ClearPset(hObject, 'PSet_WallCommon')
```

```pascal
resultOK := IFC_ClearPset(hObject, 'Example');
```
```python
import vs

# Removes a Property Set from the object's attached Ifc Record.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
inStrPsetName = 'Example'

ok = vs.IFC_ClearPset(hObject, inStrPsetName)
if ok:
    vs.Message('IFC_ClearPset succeeded')
else:
    vs.Message('IFC_ClearPset failed')
```

## Version
Available from: Vectorworks 2016

## Category
* [IFC](../Categories/IFC.md)
