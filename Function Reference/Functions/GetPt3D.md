# GetPt3D

## Description
Procedure GetPt3D switches the cursor to 3D selection mode and allows the user to select a point in a VectorWorks document. This cannot be used if there is a function anywhere in the calling chain.

```pascal
PROCEDURE GetPt3D(
				VAR pX, pY, pZ : REAL;
				useWPOnly      : BOOLEAN);
```

```python
def vs.GetPt3D(useWPOnly, callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pX, pY, pZ|REAL|Returns coordinates of mouse click.|
|useWPOnly|BOOLEAN|TRUE if the returned point have to be on the active Working Plane. Snapping to arbitrary 3D geometry will produce vertical projection result on the WP; FALSE if the point can be arbitrary 3D point (produced, for example, by snapping to a 3D geometry)|

## Remarks
(*_c_*, 2011.01.09) the z-value of the returned 3D point is always zero if 
* the current view is Top-plan or Top (From Raymond Mullin). 
* there is no pre-existing snapped geometry in 3D (by useWPOnly = FALSE)

In Python this function will _NOT_ block execution. It will execute a callback function with the resulted point (as callback function parameter).

## Examples
on sample is similar to the sample in [GetPt](GetPt.md).

## See Also
VS Functions:
[GetPt](GetPt.md) |
[GetPtL](GetPtL.md) |
[GetPt3D](GetPt3D.md) |
[GetPtL3D](GetPtL3D.md) |
[GetLine](GetLine.md) |
[GetLine3D](GetLine3D.md) |
[GetRect](GetRect.md) |
[GetRect3D](GetRect3D.md) |
[TrackObject](TrackObject.md)

## Version
Availability: from Vectorworks 2010

## Category
* [User Interactive](../Categories/User%20Interactive.md)
