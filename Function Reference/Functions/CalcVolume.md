# CalcVolume

## Description
Function CalcVolume calculates the volume of the referenced solid object. The function supports only valid solids objects.

```pascal
FUNCTION CalcVolume(solidObject : HANDLE): REAL;
```

```python
def vs.CalcVolume(solidObject):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|solidObject|HANDLE|Handle to solids object.|

## Remarks
Calculates the volume of the given object if a valid solid.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
volume, area: REAL;
BEGIN
IF FSActLayer <> NIL THEN BEGIN
volume := CalcVolume(FSActLayer);
area := CalcSurfaceArea(FSActLayer);
Message('Volume ', volume, ', surface area ', area);
END;
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	if vs.FSActLayer() != None:
		volume = vs.CalcVolume(vs.FSActLayer())
		area = vs.CalcSurfaceArea(vs.FSActLayer())
		vs.Message('Volume ', volume, ', surface area ', area)
Example()
```

## Version
CalcVolume is obsolete as of VectorWorks12.5<P>


Availability: from VectorWorks8.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
