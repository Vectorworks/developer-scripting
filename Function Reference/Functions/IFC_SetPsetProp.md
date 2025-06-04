# IFC_SetPsetProp

## Description
This function sets a value to the selected property of the selected pset.

```pascal
FUNCTION IFC_SetPsetProp(
				hObject        : HANDLE;
				inStrPsetName  : STRING;
				inStrPropName  : STRING;
				inStrPropValue : STRING): BOOLEAN;
```

```python
def vs.IFC_SetPsetProp(hObject, inStrPsetName, inStrPropName, inStrPropValue):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to object|
|inStrPsetName|STRING|Name of the pset|
|inStrPropName|STRING|Name of the property|
|inStrPropValue|STRING|Value of the property|

## Examples
Assume we have a wall and we want in export to be marked as load-bearing, non-combustible and to put a reference ‘IW-01’, also we want to set thermal transmit-tance value of 0.5 – we need to attach Pset_WallCommon and set its properties ( LoadBearing, Combustible, Reference, ThermalTransmittance) as needed:
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	hWall : HANDLE;
	ok : BOOLEAN;
BEGIN
	hWall := FSActLayer;
	ok := IFC_SetIFCEntity(hWall, 'IfcWallStandardCase');
	ok := IFC_AttachPset(hWall, 'Pset_WallCommon');
	ok := IFC_SetPsetProp(hWall, 'Pset_WallCommon', 'LoadBearing', '1');
	ok := IFC_SetPsetProp(hWall, 'Pset_WallCommon', 'Combustible', '0');
	ok := IFC_SetPsetProp(hWall, 'Pset_WallCommon', 'Reference', 'IW-01');
	ok := IFC_SetPsetProp(hWall, 'Pset_WallCommon', 'ThermalTransmittance', '0.5');
END;

RUN(Test);
```
#### Python ####
```python
hWall = vs.FSActLayer()
ok = vs.IFC_SetIFCEntity(hWall, 'IfcWallStandardCase')
ok = vs.IFC_AttachPset(hWall, 'Pset_WallCommon')
ok = vs.IFC_SetPsetProp(hWall, 'Pset_WallCommon', 'LoadBearing', '1')
ok = vs.IFC_SetPsetProp(hWall, 'Pset_WallCommon', 'Combustible', '0')
ok = vs.IFC_SetPsetProp(hWall, 'Pset_WallCommon', 'Reference', 'IW-01')
ok = vs.IFC_SetPsetProp(hWall, 'Pset_WallCommon', 'ThermalTransmittance', '0.5')
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
