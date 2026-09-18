# Cloud

## Description
Draws a cloud. Varies the billows of the clouds randomly between rMin and rMax. The hFactor is the height of each individual arc in the cloud.

```pascal
FUNCTION Cloud(
				h                   : HANDLE;
				rMin                : REAL;
				rMax                : REAL;
				hFactor             : REAL;
				convex              : BOOLEAN;
				removeIntersections : BOOLEAN): HANDLE;
```

```python
def vs.Cloud(h, rMin, rMax, hFactor, convex, removeIntersections):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|rMin|REAL|   |
|rMax|REAL|   |
|hFactor|REAL|   |
|convex|BOOLEAN|   |
|removeIntersections|BOOLEAN|   |

## Examples
```pascal
		ArcTo(0 * Scale, .375 * Scale, 0 * Scale);
	EndPoly;
	h3 := LNewObj;
	{! Trying to run the Cloud routine on a rectangle produces a memory error.}
	h4 := Cloud(h3, (.06" * containerScale), (.11" * containerScale), .625, TRUE, FALSE);
	DelObj(h3);
	textCenterY := 0;
END ELSE IF pConfig = 'Data' THEN BEGIN
	BeginPoly;

	BEGIN
		Rect (x1, y1, x2, y2);
		tempH := LNewObj;
{		CloudNine := Cloud (tempH, rMin * layerScale, rMax * layerScale, kHFactor, TRUE, TRUE);}
		CloudNine := Cloud (tempH, rMin * layerScale, rMax * layerScale, kHFactor, TRUE, FALSE); {changed to fix MacOS9 fatal -- RFA}
		DelObject (h);
		DelObject (tempH);
	END

		IF (polyH <> NIL) THEN
{			cloudH := cloud (polyH, rMin, rMax, hFactor, convex, TRUE)}
			cloudH := cloud (polyH, rMin, rMax, hFactor, convex, FALSE) {Changed 3/8/04 to fix MacOS9 fatal--RFA}
		ELSE SysBeep;
```
```python
import vs

# Draws a cloud.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
rMin = 1.0
rMax = 2.0
hFactor = 1.0
convex = True
removeIntersections = True

objHandle = vs.Cloud(h, rMin, rMax, hFactor, convex, removeIntersections)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
