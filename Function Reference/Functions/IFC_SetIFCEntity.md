# IFC_SetIFCEntity

## Description
This function creates and attaches to hObject an IFC Record with the given IFC entity.

```pascal
FUNCTION IFC_SetIFCEntity(
				hObject      : HANDLE;
				inStrIfcName : STRING): BOOLEAN;
```

```python
def vs.IFC_SetIFCEntity(hObject, inStrIfcName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|
|inStrIfcName|STRING|Name of the IFC entity|

## Examples
Assume we have an object, which we want to be exported as furniture:
#### VectorScript ####
```pascal
IFC_SetIFCEntity(hObject, ‘IfcFurnishingElement’);
```
#### Python ####
```python
ok = vs.IFC_SetIFCEntity(hObject, ‘IfcFurnishingElement’)
```

```pascal
resultOK := IFC_SetIFCEntity(hObject, 'Example');
```
```python
import vs

# This function creates and attaches to hObject an IFC Record with the given
# IFC entity.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
inStrIfcName = 'Example'

ok = vs.IFC_SetIFCEntity(hObject, inStrIfcName)
if ok:
    vs.Message('IFC_SetIFCEntity succeeded')
else:
    vs.Message('IFC_SetIFCEntity failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
