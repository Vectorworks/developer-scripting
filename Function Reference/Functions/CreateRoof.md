# CreateRoof

## Description
Function CreateRoof creates a new roof object in a VectorWorks document, returning a handle to the object. To define the roof object template, use [AppendRoofEdge](AppendRoofEdge.md).

**Table - Roof Miter Styles**

| Miter Style | Constant |
|-------------|----------|
| Vertical    | 1        |
| Horizontal  | 2        |
| Double      | 3        |
| Square      | 4        |

```pascal
FUNCTION CreateRoof(
				genGableWall         : BOOLEAN;
				bearingInsetDistance : REAL;
				roofThickDistance    : REAL;
				miterType            : INTEGER;
				vertMiterDistance    : REAL): HANDLE;
```

```python
def vs.CreateRoof(genGableWall, bearingInsetDistance, roofThickDistance, miterType, vertMiterDistance):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|genGableWall|BOOLEAN|Specifies gable roof generation.|
|bearingInsetDistance|REAL|Bearing inset distance of wall into roof.|
|roofThickDistance|REAL|Roof thickness.|
|miterType|INTEGER|Miter style of roof.|
|vertMiterDistance|REAL|Vertical component for double miters.|

## Remarks
Use [AppendRoofEdge](AppendRoofEdge.md)() to define the roof plan.
genGableWall: Create wall object on gable ends, otherwise no wall is created.
bearingInset is where the weight of the roof rests on the wall.  This is an inset from the defining edge of the roof plan.
miterType:  1: vertical miter, 2: horizontal miter, 3: double miter , 4: square miter
vertMiter: Specifies vertical len of double miter.

## Examples
[CreateRoofObj](examples/CreateRoofObj.md)

## See Also
VS Functions:
[AppendRoofEdge](AppendRoofEdge.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
