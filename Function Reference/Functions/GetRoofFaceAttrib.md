# GetRoofFaceAttrib

## Description
Returns information on the referenced roof face object.

**Table - Roof Miter Styles**

| Miter Style | Constant |
|-------------|----------|
| Vertical    | 1        |
| Horizontal  | 2        |
| Double      | 3        |
| Square      | 4        |

```pascal
PROCEDURE GetRoofFaceAttrib(
				roofFace      : HANDLE;
				VAR roofRise  : REAL;
				VAR roofRun   : REAL;
				VAR miterType : INTEGER;
				VAR holeStyle : INTEGER;
				VAR vertPart  : REAL;
				VAR thickness : REAL);
```

```python
def vs.GetRoofFaceAttrib(roofFace):
    return (roofRise, roofRun, miterType, holeStyle, vertPart, thickness)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofFace|HANDLE|Handle to roof face object.|
|roofRise|REAL|Rise of roof.|
|roofRun|REAL|Run of roof.|
|miterType|INTEGER|Miter style of roof.|
|holeStyle|INTEGER|Miter style of openings.|
|vertPart|REAL|Vertical component of compound miters.|
|thickness|REAL|Thickness of roof.|

## Remarks
*\_c\_*, 2015.12.18: 
Hole style of openings:
: 1 Vertical
: 3 Splayed
: 4 Square Cut

Other authors:
* Returns information about old-style roof objects (single roof faces).
* Returns slope, edge miter style, miter dimensions, and thickness of roof object.

See Also [ GetRoofFaceCoords](GetRoofFaceCoords.md)() for additional roof face data

## Examples
[GetRoofProperties](examples/GetRoofProperties.md)

```pascal
GetRoofFaceAttrib(roofFace, 1.0, 2.0, 1, 2, 0.5, 1.5);
```
```python
import vs

# Returns information on the referenced roof face object.
roofFace = vs.FSActLayer()  # handle to the first selected object on the active layer

roofRise, roofRun, miterType, holeStyle, vertPart, thickness = vs.GetRoofFaceAttrib(roofFace)
vs.Message('GetRoofFaceAttrib returned: ' + str((roofRise, roofRun, miterType, holeStyle, vertPart, thickness)))
```

## Version
Availability: from VectorWorks 9.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
