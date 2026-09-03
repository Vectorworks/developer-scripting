# HMoveBackward

## Description
Move the referenced object backward in the object stacking order. If toBack is TRUE, the object will be moved to the back of the stacking order.

```pascal
PROCEDURE HMoveBackward(
				h      : HANDLE;
				toBack : BOOLEAN);
```

```python
def vs.HMoveBackward(h, toBack):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|toBack|BOOLEAN|Move to back of stacking order.|

## Remarks
It is possible using HMoveForward and HMoveBackward to re-order layers. But use caution. Do not set the toBack argument to TRUE -- it will delete the layer. Also, Peter Vandewalle claims that the layer can get deleted even if toBack is FALSE, if you keep sending it backward. (I could not confirm this.)

## Examples
```pascal
	SetLW(LNewObj,kThinLine);
IF IsLineStyleByClass THEN SetLSByClass( LNewObj );
HMoveBackward(LNewObj, TRUE);
MoveTo(X,Y);
LineTo(X,Y+Length);
	IF IsLineStyleByClass THEN SetLSByClass( LNewObj );
LineTo(X+Depth+Overhang,Y+Length);

IF pBox THEN BEGIN
	Rect(x1-margin,y1+margin,x2+margin,y2-margin);
	hBox := LNewObj;
	HMoveBackward(LNewObj,FALSE);
END;

		Relative;
		Rect (-boxW/2, boxH/2, boxW/2, -boxH/2);
		SetPenFore (LNewObj, 65535, 0, 0);
		SetFPat (LNewObj, 1);
		HMoveBackward (LNewObj, TRUE);
	EndGroup;
	HMoveForward (LNewObj, TRUE);
END;	{of createErrorMessage2}
```
```python
vs.Rect( kBf * b1[0], kBf * b1[1], kBf * b2[0], kBf * b2[1] )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 1 )
vs.HMoveBackward( vs.LNewObj(), False )
vs.EndGroup()
vs.HMoveForward( vs.LNewObj(), True )

vs.AddPoint( vs.PThroat_Width + vs.PCurb_Width + rightFence, -gMinFenceOffset )
vs.EndPoly()
vs.HMoveBackward( vs.LNewObj(), True )
vs.SetFenceAttrs( vs.LNewObj() )
```

## Version
Availability: from VectorWorks8.5

## Category
* [Object Editing](../Categories/Object%20Editing.md)
