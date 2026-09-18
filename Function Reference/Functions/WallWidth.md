# WallWidth

## Description
Function WallWidth returns the wall width of the referenced wall object.

```pascal
FUNCTION WallWidth(wallHd : HANDLE): REAL;
```

```python
def vs.WallWidth(wallHd):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHd|HANDLE|Handle to wall.|

## Remarks
"Function WallWidth returns the wall width of the referenced wall object", whereas [HWallWidth](HWallWidth.md) changes the width of the referenced wall. [GetWallThickness](GetWallThickness.md)(wallHandle, thicknessDist) 

(http://www.nemetschek.net/support/custom/vscript/reference/asp/main.asp?name=GetWallThickness) does the same as WallWidth, but is often more practical and at least looks better in scripts.

## Examples
```pascal
	lngth := Distance(beg_pt.x, beg_pt.y, END_pt.x, END_pt.y);
	lngth := lngth + pAdd_to_Start + pAdd_to_END;
	beg_pt := WorldToObjectCoords(pluginH, beg_pt);
	originX := beg_pt.x - pAdd_TO_Start;
	originY := beg_pt.y + offset - (WallWidth(wallH) / 2);
END;

		END;
	END;
	temp3_h := NextObj(temp3_h);
END;
line_v := UnitVec(END_small - beg_small) * WallWidth(wall_h) / 4;
beg_pt := ((beg_small + beg_large) / 2) - line_v;
END_pt := ((END_small + END_large) / 2) + line_v;
IF Dist(beg_pt, END_pt) < Dist(wall_beg_pt, END_pt) THEN beg_pt := wall_beg_pt;
IF Dist(END_pt, beg_pt) < Dist(wall_END_pt, beg_pt) THEN end_pt := wall_end_pt;

if NOT dimToCoreComp THEN BEGIN
	tJoins[tJoin_cnt].wallWidth := WallWidth(wall_h);
	tJoins[tJoin_cnt].wallStartPt := beg_pt;
	tJoins[tJoin_cnt].wallEndPt := END_pt;
	tJoins[tJoin_cnt].tJoinPt := breakTestPt;
END ELSE BEGIN
```
```python
import vs

# Function WallWidth returns the wall width of the referenced wall object.
wallHd = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.WallWidth(wallHd)
vs.Message('WallWidth returned: ' + str(value))
```

## See Also
VS Functions:
[GetWallThickness](GetWallThickness.md) 
| [HWallWidth](HWallWidth.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
