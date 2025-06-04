# ObjSurfaceArea

## Description
Function ObjSurfaceArea calculates the surface area of the referenced solid object. The function supports only valid solids objects.

```pascal
FUNCTION ObjSurfaceArea(solidObject : HANDLE): REAL;
```

```python
def vs.ObjSurfaceArea(solidObject):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|solidObject|HANDLE|Handle to solids object.|

## Remarks
Calculates the volume of the given object if a valid solid.




Apparently this command is replacing CalcSurfaceArea. It should be noted that ObjSurfaceArea returns the surface area in area units from the Units dialog. CalcSurfaceArea returns the volume in length units squared.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
volume, area: REAL;
BEGIN
IF FSActLayer &lt;&gt; NIL THEN BEGIN
volume := CalcVolume(FSActLayer);
area := CalcSurfaceArea(FSActLayer);
Message('Volume ', volume, ', surface area ', area);
END;
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks12.5

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
