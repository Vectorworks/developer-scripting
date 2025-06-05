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
*_c_*, 2015.12.18: 
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

## Version
Availability: from VectorWorks 9.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
