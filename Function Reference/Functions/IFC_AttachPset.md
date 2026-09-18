# IFC_AttachPset

## Description
Attaches a property set to the object

```pascal
FUNCTION IFC_AttachPset(
				hObject       : HANDLE;
				inStrPsetName : STRING): BOOLEAN;
```

```python
def vs.IFC_AttachPset(hObject, inStrPsetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|
|inStrPsetName|STRING|of the pset|

## Examples
Assume we want an object to be exported as a space with attached  Pset_SpaceFireSafetyRequirements (first we have to attach IfcSpace with mandatory and enumerational properties and then the pset):
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	hSpace : HANDLE;
	ok : BOOLEAN;
begin
	ok := IFC_SetIFCEntity(hSpace, 'IfcSpace');
	ok := IFC_SetEntityProp(hSpace, 'CompositionType', 'ELEMENT');
	ok := IFC_SetEntityProp(hSpace, 'InteriorOrExteriorSpace', 'INTERIOR');
	ok := IFC_AttachPset(hSpace, 'Pset_SpaceFireSafetyRequirements');
END;

RUN(Test);
```
#### Python ####
```python
hSpace = vs.FSActLayer()
ok = vs.IFC_SetIFCEntity(hSpace, 'IfcSpace')
ok = vs.IFC_SetEntityProp(hSpace, 'CompositionType', 'ELEMENT')
ok = vs.IFC_SetEntityProp(hSpace, 'InteriorOrExteriorSpace', 'INTERIOR')
ok = vs.IFC_AttachPset(hSpace, 'Pset_SpaceFireSafetyRequirements')
```

```pascal
resultOK := IFC_AttachPset(hObject, 'Example');
```
```python
import vs

# Attaches a property set to the object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
inStrPsetName = 'Example'

ok = vs.IFC_AttachPset(hObject, inStrPsetName)
if ok:
    vs.Message('IFC_AttachPset succeeded')
else:
    vs.Message('IFC_AttachPset failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
