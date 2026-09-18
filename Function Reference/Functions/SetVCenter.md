# SetVCenter

## Description
Procedure SetVCenter sets the VectorWorks document view center.

```pascal
PROCEDURE SetVCenter(viewCenterX,viewCenterY : REAL);
```

```python
def vs.SetVCenter(viewCenter):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewCenter|REAL|Coordinates of document view center.|

## Examples
#### VectorScript ####
```pascal
SetVCenter(2,4);
```
#### Python ####
```python

```

```pascal
		Layer(gSheetInfoList[i,10])
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

BEGIN
	SetPrefReal( 500, DocZoomLevel );
	SetVCenter( DocViewCenter.x, DocViewCenter.y );
	Redraw;		{//// Fix for VB-178895 Camera Match Tune View: View not live updating while slider is moving. }
END;
```
```python
vs.SetVCenter(viewCenter)
```

## Version
Availability: from MiniCAD6.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
