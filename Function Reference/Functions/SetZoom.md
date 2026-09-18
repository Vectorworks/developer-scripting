# SetZoom

## Description
Procedure SetZoom sets the zoom factor of the active VectorWorks document.

```pascal
PROCEDURE SetZoom(zoomfactor : LONGINT);
```

```python
def vs.SetZoom(zoomfactor):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|zoomfactor|LONGINT|Zoom percentage setting.|

## Examples
```pascal
	IF (container_tp = 11) {I'm in a group}
		THEN temp_b := GetPickObjectInfo(pt1.x,pt1.y,gGroupH,gLine,temp_i)
		ELSE BEGIN
			zoomF := GetZoom;
			SetZoom (100000);
			gLine := PickObject(pt1.x,pt1.y);
			SetZoom (zoomF);
{
message (' *** pt1.x = ',pt1.x,'    pt1.y = ',pt1.y,'    gLine = ',gLine, '(',gettype(gLine),')', '    gParmH = ',gParmH, '(',gettype(gParmH),')');

	{if gSheetInfoList[i,10] is a saved view}
	ELSE IF (GetType (GetObject (gSheetInfoList[i,10])) = 49) THEN
		VRestore(gSheetInfoList[i,10]);
	SetVCenter (gCenterX,gCenterY);
	SetZoom (gZoomFactor);
END;

BEGIN
	Layer (GetLName (GetParent (gBorderH [sheetNum])));
	SetVCenter (gCenterX,gCenterY);
	SetZoom (gZoomFactor);
END;
```
```python
import vs

# Procedure SetZoom sets the zoom factor of the active VectorWorks document.
zoomfactor = 1

vs.SetZoom(zoomfactor)
```

## Version
Availability: from MiniCAD6.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
