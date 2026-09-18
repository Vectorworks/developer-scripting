# SetFenceAttrs

## Description
Applies fence attributes to input handle.

```pascal
PROCEDURE SetFenceAttrs(fFenceHandle : HANDLE);
```

```python
def vs.SetFenceAttrs(fFenceHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fFenceHandle|HANDLE|   |

## Examples
```pascal
	IF (bCanContinue) THEN
		gTempH := OffsetPoly(gMyPolygon,pFence_offset,1,TRUE,TRUE,kRez,0.25" )
	ELSE
		gTempH := gMyPolygon;
SetFenceAttrs(gTempH);
SetFPat(lnewobj,0);
END;

		DrawRoadway2D(-CurbOutside-gLFO,1);
		DrawRoadway2D(CurbOutside+gRFO,-1);
	EndPoly;
	HMoveBackward(LNewObj,TRUE);
	SetFenceAttrs(LNewObj);
END;	{ If ShowFence }

SetFenceAttrs(h1);
```
```python
vs.EndPoly()
vs.HMoveBackward( vs.LNewObj(), True )
vs.SetFenceAttrs( vs.LNewObj() )
vs.Locus( vs.PRadius + vs.PCurb_Width + ( vs.PWidth / 2 ), 0 ); SetAttrsByClassOrParent( vs.LNewObj(), gObjHandle, gCurb_Class )
vs.Rotate( -angDTMMod / 2 )
vs.DSelectAll()

vs.AddPoint( length + gMinFenceOffset, -( width + vs.PCurb_Width + vs.PRight_Fence_Offset ) )
vs.AddPoint( -gMinFenceOffset, -( width + vs.PCurb_Width + vs.PRight_Fence_Offset ) )
vs.EndPoly()
vs.SetFenceAttrs( vs.LNewObj() )

vs.AddPoint( vs.PThroat_Width + vs.PCurb_Width + rightFence, -gMinFenceOffset )
vs.EndPoly()
vs.HMoveBackward( vs.LNewObj(), True )
vs.SetFenceAttrs( vs.LNewObj() )
```

## Version
Availability: from Vectorworks 2015

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
