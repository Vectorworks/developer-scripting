# SetView

## Description
Procedure SetView sets the view of a VectorWorks document. The projection must be non-plan to modify the view.

```pascal
PROCEDURE SetView(
				xAngle    : REAL;
				yAngle    : REAL;
				zAngle    : REAL;
				xDistance : REAL;
				yDistance : REAL;
				zDistance : REAL);
```

```python
def vs.SetView(xAngle, yAngle, zAngle, xDistance, yDistance, zDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|xAngle|REAL|X axis rotation angle.|
|yAngle|REAL|Y axis rotation angle.|
|zAngle|REAL|Z axis rotation angle.|
|xDistance|REAL|X coordinate of view center.|
|yDistance|REAL|Y coordinate of view center.|
|zDistance|REAL|Z coordinate of view center.|

## Remarks
Listed example generates VectorScript error due to the units designation after the view angle.



Works for me. Is this a Mac-only problem?



You can also set the view to one of the standard views, like this:
<code lang="pas">
PROCEDURE Example;
CONST
kViewTopPlan        = 1;
kViewTop            = 2;
kViewFront          = 3;
kViewRight          = 4;
kViewBottom         = 5;
kViewBack           = 6;
kViewLeft           = 7;
kViewRightIso       = 8;
kViewLeftIso        = 9;
kViewRightRearIso   = 10;
kViewLeftRearIso    = 11;
kViewLowerRightIso  = 12;
kViewLowerLeftIso   = 13;
kViewLowerRightRear = 14;
kViewLowerLeftRear  = 15;
BEGIN
DoMenuTextByName('Standard Views', IntDialog('Enter a number (1~15): ', '1'));
END;
RUN(Example);
</code>

## Examples
#### VectorScript ####
```pascal
SetView(45d,30d,30d,0,2,2);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
