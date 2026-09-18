# EqPercent

## Description
Returns TRUE if num1 and num2 are equal within the given percent.

```pascal
FUNCTION EqPercent(
				value1  : REAL;
				value2  : REAL;
				percent : REAL): BOOLEAN;
```

```python
def vs.EqPercent(value1, value2, percent):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|value1|REAL|   |
|value2|REAL|   |
|percent|REAL|   |

## Examples
```pascal
But it's too late in the 10 cycle to change the interfaces, and I'm not sure
if one factor would DO it, or IF it would take more than one.}
cen_pt := ThreePtCenter(pt1, pt2, pt3);
rad := Dist(cen_pt, pt1);
IF ((EqPercent(Dist((pt1 + pt2) / 2, cen_pt), rad, 4)) &
	 (EqPercent(Dist((pt2 + pt3) / 2, cen_pt), rad, 4)) &
	 (EqPercent(Dist(pt1, pt2), Dist(pt2, pt3), 50))) THEN BEGIN
	verts[temp1-2].tipe     := 3;
	verts[temp1-2].offset   := rad;
	verts[temp1-2].center   := cen_pt;
	verts[temp1-2].startAng := Vec2Ang360(pt1 - cen_pt);
	verts[temp1-2].sweepAng := GetAngBet180(pt1, cen_pt, pt3);
```
```python
import vs

# Returns TRUE if num1 and num2 are equal within the given percent.
value1 = 1.0
value2 = 2.0
percent = 0.5

ok = vs.EqPercent(value1, value2, percent)
if ok:
    vs.Message('EqPercent succeeded')
else:
    vs.Message('EqPercent failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
