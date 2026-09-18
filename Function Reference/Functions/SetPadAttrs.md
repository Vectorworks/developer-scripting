# SetPadAttrs

## Description
Applies pad attributes to input handle.

```pascal
PROCEDURE SetPadAttrs(hPadHandle : HANDLE);
```

```python
def vs.SetPadAttrs(hPadHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hPadHandle|HANDLE|   |

## Examples
```pascal
BEGIN
gTempH := Make3DPolyAtZero(gMyPolygon,TRUE);
SetPadAttrs(gTempH);
IF gUseFence THEN
	BEGIN
		IF (bCanContinue) THEN
			gTempH := OffsetPoly(gMyPolygon,pFence_offset,1,TRUE,TRUE,kRez,0.25" )

	Draw3D(0,CurbOutside,1);
	Draw3D(0,-CurbOutside,-1);
EndPoly3D;
HMoveForward(LNewObj,TRUE);
IF ShowPad THEN SetPadAttrs(LNewObj);

	for cnt := 1 to vertCnt DO BEGIN
		NurbsSetPt3D(h3, cnt - 1, 0, left[cnt].x, left[cnt].y, left[cnt].z);
		NurbsSetPt3D(h3, cnt - 1, 1, rght[cnt].x, rght[cnt].y, rght[cnt].z);
	END;
	SetPadAttrs( h3 );
END;
```
```python
vs.EndPoly3D()
vs.SetPadAttrs( vs.LNewObj() )

vs.Add3DPt( length, -( width + vs.PCurb_Width + gDTM ), vs.PRise )
vs.Add3DPt( 0, -( width + vs.PCurb_Width + gDTM ), 0 )
vs.EndPoly3D()
vs.SetPadAttrs( vs.LNewObj() )

vs.Add3DPt( vs.PThroat_Width + vs.PCurb_Width, 0, vs.PRise )
vs.EndPoly3D()
vs.HMoveBackward( vs.LNewObj(), True )
vs.SetPadAttrs( vs.LNewObj() )
```

## Version
Availability: from Vectorworks 2015

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
