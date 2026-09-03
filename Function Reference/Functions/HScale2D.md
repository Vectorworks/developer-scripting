# HScale2D

## Description
Scales a 2D object.

```pascal
PROCEDURE HScale2D(
				h         : HANDLE;
				centerX   : REAL;
				centerY   : REAL;
				scaleX    : REAL;
				scaleY    : REAL;
				scaleText : BOOLEAN);
```

```python
def vs.HScale2D(h, centerX, centerY, scaleX, scaleY, scaleText):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|centerX|REAL|   |
|centerY|REAL|   |
|scaleX|REAL|   |
|scaleY|REAL|   |
|scaleText|BOOLEAN|   |

## Remarks
If (scaleX = -1) or (scaleY = -1) the object will be mirrored.

If used on an extrude, the 2D shape inside the extrude will be scaled. The scaling will follow the 2D shape's working plane.

[Ptr 07/17/2019]

## Examples
```pascal
SetFPat(lnewobj,0);
temp_h := lnewobj;
EndGroup;
temp_h := getparent(temp_h);
HScale2D(temp_h,0,0,0.666666667,0.108108108,FALSE);
IF (ht < wd) THEN
	BEGIN
	HRotate(temp_h, 0, 0, 90.0);
	HScale2D(temp_h,0,0,wd,ht,FALSE);

SetOpacity(LNewObj, 50);
EndGroup;
LinkSymbol := LNewObj;
HRotate(LinkSymbol,0,0,rot);
HScale2D(LinkSymbol,0,0,scale,scale,FALSE);
hmove(LinkSymbol,x,y);
MakeLinkSymbol := LinkSymbol;
END;

BEGIN
HScale2D(h,0,0,-1,1,TRUE);
fliphoriz := FALSE;
END;
```
```python
planarRef = vs.GetPlanarRef( hDuplicated )
vs.SetPlanarRef( hDuplicated, 0 )
vs.HScale2D( hDuplicated, 0, 0, dMarkerScale, dMarkerScale, True)
vs.SetPlanarRef( hDuplicated, planarRef )
```

## Version
Availability: from Vectorworks 2014

## Category
* [Object Editing](../Categories/Object%20Editing.md)
