# SetWallHeights

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See architectural category for replacement:
:[[VS:DelObjStoryBound|DelObjStoryBound]]
:[[VS:DelObjStoryBounds|DelObjStoryBounds]]
:[[VS:GetObjBoundElevation|GetObjBoundElevation]]
:[[VS:GetObjStoryBound|GetObjStoryBound]]
:[[VS:GetObjStoryBoundsAt|GetObjStoryBoundsAt]]
:[[VS:GetObjStoryBoundsCnt|GetObjStoryBoundsCnt]]
:[[VS:GetStoryLayerInfo|GetStoryLayerInfo]]
:[[VS:HasObjStoryBound|HasObjStoryBound]]
:[[VS:HasObjStoryBounds|HasObjStoryBounds]]
:[[VS:SetObjectStoryBound|SetObjectStoryBound]]

Sets the wall heights of an unstyled wall. Will return false for a styled wall.

```pascal
FUNCTION SetWallHeights(
				h               : HANDLE;
				startHtDistance : REAL;
				endHtDistance   : REAL): BOOLEAN;
```

```python
def vs.SetWallHeights(h, startHtDistance, endHtDistance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|startHtDistance|REAL|   |
|endHtDistance|REAL|   |

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
boo :BOOLEAN;
BEGIN
CallTool(-208);
h := FSActLayer;
boo := SetWallHeights(h, 12, 23);
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks12.0
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* Objects - Walls

