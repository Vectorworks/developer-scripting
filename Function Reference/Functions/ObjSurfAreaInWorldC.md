# ObjSurfAreaInWorldC

## Description
Function ObjSurfAreaInWorldC calculates the surface area of the referenced solid object. The function supports only valid solids objects.

```pascal
FUNCTION ObjSurfAreaInWorldC(solidObject : HANDLE): REAL;
```

```python
def vs.ObjSurfAreaInWorldC(solidObject):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|solidObject|HANDLE|Handle to solids object.|

## Remarks
Calculates the surface area the given object if a valid solid.

## Examples
```python
PROCEDURE Example;
VAR
        volume, area: REAL;
BEGIN
        IF FSActLayer &lt;&gt; NIL THEN BEGIN
                volume := CalcVolume(FSActLayer);
                area := ObjSurfaceAreaInWorldCoord(FSActLayer);
                Message('Volume ', volume, ', surface area ', area);
        END;
END;
RUN(Example);
```

## Version
Availability: from Vectorworks 2023.3

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
