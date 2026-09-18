# Max

## Description
Returns the maximum of the two numbers.

```pascal
FUNCTION Max(
				val1 : REAL;
				val2 : REAL): REAL;
```

```python
def vs.Max(val1, val2):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|val1|REAL|   |
|val2|REAL|   |

## Examples
```pascal
GetBBox(title_h,x1,y1,xT1,y2);
xT1 := xT1+(xT1-x1);
GetBBox(scale_h,x1,y1,xT2,y2);
xT2 := xT2+(xT2-x1) ;
gLength := ((max(xT1,xT2)) / RealLayerScale);
END

BEGIN
	{Try to avoid creating polys with too many points}
	lineLength := gVariationLength;
	lineLength := Max(gVariationLength, HPerim(hPoly) / kMaxVertNum);

	num2 := Norm(pt2 - begPt);
	IF num1 > num2
		THEN endPt := pt1
		ELSE endPt := pt2;
	chordDist := Max(num1, num2);
	Radius_Chord_2_Delta;
	Radius_Delta_2_ArcDist;
	Radius_Delta_2_TangentDist;
END;
```
```python
import vs

# Returns the maximum of the two numbers.
val1 = 1.0
val2 = 2.0

value = vs.Max(val1, val2)
vs.Message('Max returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Math - General](../Categories/Math%20-%20General.md)
