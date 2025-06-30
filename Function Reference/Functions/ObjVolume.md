# ObjVolume

## Description
Function ObjVolume calculates the volume of the referenced solid object. The function supports only valid solids objects.

```pascal
FUNCTION ObjVolume(solidObject : HANDLE): REAL;
```

```python
def vs.ObjVolume(solidObject):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|solidObject|HANDLE|Handle to solids object.|

## Remarks
Calculates the volume of the given object if a valid solid.




Apparently this command is replacing CalcVolume. It should be noted that ObjVolume returns the volume in volume units from the Units dialog. CalcVolume returns the volume in length units cubed.

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

```

## Version
Availability: from VectorWorks12.5

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
