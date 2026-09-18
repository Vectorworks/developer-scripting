# Centroid

## Description
Returns the centroid of the object. Returns false if an unsupported object type is supplied.

```pascal
FUNCTION Centroid(
				h     : HANDLE;
				VAR x : REAL;
				VAR y : REAL): BOOLEAN;
```

```python
def vs.Centroid(h):
    return (BOOLEAN, x, y)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|x|REAL|   |
|y|REAL|   |

## Remarks
(*\_c\_* 2016.04.18): This returns mm, so convert the values into current units:
```pascal
IF Centroid(h, c.x, c.y) THEN BEGIN
        { centroid returns mm }
        c.x := c.x * GetPrefReal(152) / 25.4;
	c.y := c.y * GetPrefReal(152) / 25.4;
END;
```

## Examples
```pascal
BEGIN
	IF Centroid (objectH, gX0, gY0) THEN
	BEGIN
		gX0 := gX0 * gUPI / 25.4;
		gY0 := gY0 * gUPI / 25.4;
		Locus (gX0, gY0);
	END;

BEGIN
	IF (NOT p__Is3D) AND Centroid(LNewObj,gXC,gYC) THEN
	BEGIN
		gXC := gXC * GetPrefReal (152) / 25.4;
		gYC := gYC * GetPrefReal (152) / 25.4;
		{calculate the centorid offset from the insertion point}
		centroidOffset.x := gXC;
		centroidOffset.y := gYC;

BEGIN
	IF Centroid (LNewObj, gXC, gYC) THEN
	BEGIN
		gXC := gXC * gUPI / 25.4;
		gYC := gYC * gUPI / 25.4;
		Locus (gXC, gYC);
	END;
```
```python
import vs

# Returns the centroid of the object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, x, y = vs.Centroid(h)
vs.Message('Centroid returned: ' + str((ok, x, y)))
```
See also in tutorials: [25. Geometric Property Extraction Table](ai%20examples/25_WorksheetPolyGeometry.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
