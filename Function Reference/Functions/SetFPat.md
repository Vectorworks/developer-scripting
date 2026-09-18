# SetFPat

## Description
Procedure SetFPat sets the fill pattern of the referenced object.

To apply a bitmap fill pattern, use positive value corresponding to the index  of the bitmap pattern.  To apply a vector fill pattern, use the negative of the vector fill index (index * -1).

Fill patterns and their associated constants can be found in the [VectorScript Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
PROCEDURE SetFPat(
				h           : HANDLE;
				fillPattern : LONGINT);
```

```python
def vs.SetFPat(h, fillPattern):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|fillPattern|LONGINT|Fill index value.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE AddSurfaceExample;
VAR
	h1, h2, h3 :HANDLE;
BEGIN
	DSelectAll;
	CallTool(-203);
	h1 := FSActLayer;
	DSelectAll;
	CallTool(-203);
	h2 := FSActLayer;
	h3 := AddSurface(h1, h2);
	IF h3 <> nil THEN SetFPat(h3, 5);
END;
RUN(AddSurfaceExample);
```

#### Python ####
The python code will not pause for the execution of CallTool, that's why it uses a callback mechanism for the script to know when the temp tool has finished.

```python
# this will not be called prior Vectorworks 2022 SP3
# as the calback functions will not be executed prior to that version
def Example():
	vs.DSelectAll()

	def resultCallback1():
		h1 = vs.FSActLayer()
		vs.DSelectAll()
		
		def resultCallback2():
			h2 = vs.FSActLayer()
			h3 = vs.AddSurface(h1, h2)
			if h3 != None :  
				vs.SetFPat(h3, 5)
		
		
		vs.CallTool(-203, resultCallback2)
			
	vs.CallTool(-203, resultCallback1)

Example()
```

```pascal
				LineTo(x0 + x[i], y0 + y[i]);
		END;
	EndPoly;
	objectH := LNewObj;
	SetFPat (objectH, FFillPat);
END;	{of drawAngle}

			ELSE
				LineTo(x0 + x[i], y0 + y[i]);
		END;
	EndPoly;
	SetFPat (LNewObj, FFillPat);
END;	{of drawAngle}

BEGIN
	CreateText(theLabel);
	HCenter(LNewObj, x, y);
	HMove(LNewObj, centerPt[1]-x, centerPt[2]-y);
	SetFPat(LNewObj, 0);
	gNothingDrawn := FALSE;
END;
```
```python
vs.MoveTo ( textPtx, textPty )
vs.DSelectAll()
vs.CreateText( vs.PSheet_No )
vs.SetFPat( vs.LNewObj(), 0 )
vs.Rotate( dTextRotation )

vs.SetTextVerticalAlign( vs.LNewObj(), 3 )
vs.SetTextJust( vs.LNewObj(), 2 )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 0 )
b1, b2 = vs.GetBBox( vs.LNewObj() )
vs.Rect( kBf * b1[0], kBf * b1[1], kBf * b2[0], kBf * b2[1] )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 1 )

if t != vs.kLineNode and t != vs.kLocusNode and t != vs.kLocus3DNode and t != vs.kGroupNode:
	vs.SetFPat(objH, vs.GetFPat(parentH))
```

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
