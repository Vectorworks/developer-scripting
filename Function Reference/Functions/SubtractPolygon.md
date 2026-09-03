# SubtractPolygon

## Description
Clips one polygon from the other.

```pascal
FUNCTION SubtractPolygon(
				hMinuedPoly : HANDLE;
				hSubtrahend : HANDLE;
				dFuzz       : REAL): HANDLE;
```

```python
def vs.SubtractPolygon(hMinuedPoly, hSubtrahend, dFuzz):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hMinuedPoly|HANDLE|   |
|hSubtrahend|HANDLE|   |
|dFuzz|REAL|   |

## Examples
```pascal
HMoveBackward (LNewObj, TRUE);
ClipSurface (LNewObj, objH);
HMoveBackward (LNewObj, TRUE);
objH3 := LNewObj;
tempobjH := SubtractPolygon (objH3, objH, Fuzzer);
IF tempobjH <> NIL THEN
BEGIN
	DelObject (objH3);
	HMoveBackward (tempobjH, TRUE);
```
```python
import vs

# Clips one polygon from the other.
hMinuedPoly = vs.FSActLayer()  # handle to the first selected object on the active layer
hSubtrahend = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
dFuzz = 1.0

objHandle = vs.SubtractPolygon(hMinuedPoly, hSubtrahend, dFuzz)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
