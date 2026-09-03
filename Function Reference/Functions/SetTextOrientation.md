# SetTextOrientation

## Description
Procedure SetTextOrientation sets the position and orientation attributes of the referenced text object.

```pascal
PROCEDURE SetTextOrientation(
				theText                 : HANDLE;
				textOriginX,textOriginY : REAL;
				textAngle               : REAL;
				textIsMirrored          : BOOLEAN);
```

```python
def vs.SetTextOrientation(theText, textOrigin, textAngle, textIsMirrored):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|textOrigin|REAL|Coordinates of text object origin.|
|textAngle|REAL|Rotation angle for text object.|
|textIsMirrored|BOOLEAN|Mirroring setting for text object.|

## Examples
```pascal
		gAlignIdx := 1;
		gVAlignIdx := 3;
		END;
CreateText(nomht);
SetTextOrientation(lnewobj,0.0,ht/2,gRot,FALSE);
SetTextVerticalAlign(lnewobj,gVAlignIdx);
SetTextJust(lnewobj,gAlignIdx);
SetFPat(lnewobj,0);

SetTextOrientation(TmpTextHand, xLoc,yLoc, -GetSymRot(ActiveParmHand)+gTextRot, FALSE);

10: BEGIN	{ Text }
	getTextOrientation(hTemp, x1, y1, startA, isMirr);
	FOR ptIndex := 0 TO len(gettext(hTemp))-1 DO setTextSize(hTemp, ptIndex, 1, factor*getTextSize(hTemp, ptIndex));
	setTextOrientation(hTemp, x1*factor, y1*factor, startA, isMirr);
	END;
```
```python
import vs

# Procedure SetTextOrientation sets the position and orientation attributes
# of the referenced text object.
theText = 'Example text'
textOrigin = 'Example'
textAngle = 45.0
textIsMirrored = True

vs.SetTextOrientation(theText, textOrigin, textAngle, textIsMirrored)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
