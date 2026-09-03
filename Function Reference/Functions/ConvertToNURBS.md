# ConvertToNURBS

## Description
This function converts the input object into a new NURBS object or a group of NURBS objects in the document.

```pascal
FUNCTION ConvertToNURBS(
				h        : HANDLE;
				keepOrig : BOOLEAN): HANDLE;
```

```python
def vs.ConvertToNURBS(h, keepOrig):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle of original object.|
|keepOrig|BOOLEAN|Leave the original object in the drawing.|

## Remarks
*\_c\_* (2010.12.24) The orientation of the generated NURBS object is -like for extrudes- based on the active view. Set the plane of your profile object with [SetPlanarRefIDToGround](SetPlanarRefIDToGround.md) if you need it planar.

## Examples
[NURBSObject](examples/NURBSObject.md)

```pascal
BEGIN
	z := z + deltaZ;
	SetPlanarRefIDToGround(curveHand [cnt]);
	nurbsHand [cnt] := ConvertToNURBS(curveHand [cnt], FALSE);
	Move3DObj(nurbsHand [cnt], 0, 0, z);
END;

OpenPoly;
BeginPoly3D;
	Draw3D( Elev1, Offset, 1 );
EndPoly3D;
hCurve := ConvertToNURBS( LNewObj, FALSE );

	{ convert to NURBS curve. }
	hCurve := ConvertToNURBS( LNewObj, FALSE );
END;
```
```python
		DrawRoadway( r1, sweep2D, w )
	vs.SetZVals( zVal, deltaZVal )
vs.EndGroup()
tempHand = vs.ConvertToNURBS( vs.LNewObj(), False )
SetAttrsByClassOrParent( tempHand, gObjHandle, gPaving_Class )
#vs.SetSelect( gObjHandle )
DrawRoadway( r1, sweep2D, w )
```

## Version
Availability: from VectorWorks 10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
