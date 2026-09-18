# GetVCenter

## Description
Procedure GetVCenter returns the VectorWorks document coordinates at the center of the drawing window.

```pascal
PROCEDURE GetVCenter(VAR centerX,centerY : REAL);
```

```python
def vs.GetVCenter():
    return center
```

## Parameters
|Name|Type|Description|
|---|---|---|
|center|REAL|Returns view center point.|

## Remarks
(*\_c\_*, 2015.03.01):  This is not to be confused with the center of the page. The view center is always the center of the open window, so if you resize the window or pan somewhere else, for example, the view center will move accordingly.

## Examples

```pascal
BEGIN
	GetVCenter (gCenterX, gCenterY);
	gZoomFactor := GetZoom;

BEGIN
	GetVCenter(cenPt.x, cenPt.y);
	pt := pt - cenPt;
	pt := ((pt / GetPrefReal(152)) / GetLScale(ActLayer)) * (GetZoom / 100);
	GetScreen(x1, y1, x2, y2);
	pt.x := (x2 / 2) + ((pt.x / 13.5) * 1024) - 78;

BEGIN
	DocZoomLevel := GetPrefReal( 500 );
	GetVCenter( DocViewCenter.x, DocViewCenter.y );
END;
```
```python
import vs

# Procedure GetVCenter returns the VectorWorks document coordinates at the
# center of the drawing window.
result = vs.GetVCenter()
```

## Version
Availability: from VectorWorks 8.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
