# GetBBox

## Description
Procedure GetBBox returns the bounding box of the projection of the referenced object on the screen plane.

```pascal
PROCEDURE GetBBox(
				h           : HANDLE;
				VAR p1X,p1Y : REAL;
				VAR p2X,p2Y : REAL);
```

```python
def vs.GetBBox(h):
    return (p1, p2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|p1|REAL|Top left coordinate of bounding box.|
|p2|REAL|Bottom right coordinate of bounding box.|

## Remarks
[[User:CBM-c-|_c_]], 2017.02.24: GetBBox fails unpredictably on Roof faces when in top-plan: it returns a bounding box dependent on the axis widget and the page position of the face. Avoid the axis widget setting the view to Top, then the returned values will be correct. This is valid up to VW 2017 (bug reported).

## Version
Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
