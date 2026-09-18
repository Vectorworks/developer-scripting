# GetWallThickness

## Description
Gets the thickness of a wall

```pascal
FUNCTION GetWallThickness(
				h                 : HANDLE;
				VAR thicknessDist : REAL): BOOLEAN;
```

```python
def vs.GetWallThickness(h):
    return (BOOLEAN, thicknessDist)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|thicknessDist|REAL|   |

## Remarks
Same functionality as WallWidth(h), except that GetWallThickness returns also a Boolean, which may help in program flow branching.

## Examples
```pascal
BEGIN
	GetUnits( fraction, display, format, upi, unitName, unitSqName );
	factor			:= upi / 25.4;
	result			:= GetWallThickness( wallHandle, height );
	width			:= ( Str2Num( GetRField( objectHandle, objectName, 'DoorWidth' ) ) * factor );
	extrudeHeight	:= ( Str2Num( GetRField( objectHandle, objectName, 'DoorHeight' ) ) * factor );
```
```python
import vs

# Gets the thickness of a wall.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, thicknessDist = vs.GetWallThickness(h)
vs.Message('GetWallThickness returned: ' + str((ok, thicknessDist)))
```
See also in tutorials: [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
