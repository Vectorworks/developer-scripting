# CalcPolySegLen

## Description
Calculate the length between two segments of a polygon or polyline

```pascal
FUNCTION CalcPolySegLen(
				hPoly : HANDLE;
				i1    : INTEGER;
				i2    : INTEGER): REAL;
```

```python
def vs.CalcPolySegLen(hPoly, i1, i2):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hPoly|HANDLE|   |
|i1|INTEGER|   |
|i2|INTEGER|   |

## Examples
```pascal
Length := (CalcPolySegLen(GetCustomObjectPath(ghParm),1,3));
ArcCentVec := ThreePtCenter (StartWhole,MidWhole,EndWhole);

BEGIN
	GoodsTTLLength := CalcPolySegLen(hGoodsLoc,0,0)+gDrpOverlap;
	gOverlapComp := gDrpOverlap;
END

LocChainLength := CalcPolySegLen(hPreNURBSPolyLine,1,GetVertNum(hPreNURBSPolyLine));
ChainLinkTotal := LocChainLength/LocLinkPitch;
IF ChainLinkTotal < 1 THEN ChainLinkTotal := 1;
```
```python
import vs

# Calculate the length between two segments of a polygon or polyline.
hPoly = vs.FSActLayer()  # handle to the first selected object on the active layer
i1 = 1
i2 = 2

distance = vs.CalcPolySegLen(hPoly, i1, i2)
vs.Message('CalcPolySegLen returned: ' + str(distance))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
