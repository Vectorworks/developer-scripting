# Rotate3D

## Description
Procedure Rotate3D rotates the most recently created three-dimensional object. Rotation values are applied about the respective axes.

```pascal
PROCEDURE Rotate3D(
				xAngle : REAL;
				yAngle : REAL;
				zAngle : REAL);
```

```python
def vs.Rotate3D(xAngle, yAngle, zAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|xAngle|REAL|Rotation about X-axis.|
|yAngle|REAL|Rotation about Y-axis|
|zAngle|REAL|Rotation about Z-axis.|

## Remarks
From Julian:
Rotate3D() can only be called after object creation. Duplication does not count as a newly created object, so use Set3DRot() instead. If you are rotating in more than one axis, you may need to use it 3 times, first Z, then Y then X rotation.

## Examples
#### VectorScript ####
```pascal
BeginXtrd(0&quot;,4&quot;);
Rect(0&quot;,3&quot;,1&quot;,0&quot;);
EndXtrd;
Rotate3D(21d 10' 22&quot;,-18d 44' 50&quot;,-7d 5' 45&quot;);
```
#### Python ####
```python

```

```pascal
BeginXtrd(0,3*upi);
	FillBack(65535,65535,65535);
	Oval(-(0.35*cWidth),(0.35*cWidth),(0.35*cWidth),-(0.35*cWidth));
EndXtrd;
Rotate3D(xrot,yrot,zrot);
Move3Dobj(lnewobj,xtr,ytr,ztr);
BeginXtrd(6*upi,9*upi);
	FillBack(0,0,0);
	Rect(-1*upi,.35*cWidth-3*upi,1*upi,-3*upi);

	8.54167e-1',-1.3333e0'
	);
EndXtrd;
ResetOrientation3D;
Rotate3D(#0.0,#0.0,#0.0);
Move3D(0e0',0e0',0e0');
BeginXtrd(-7.1875e-1',7.1875e-1');
	Poly(
	-1.35688e0',1.5625e0',

		Rect(0,0,gDrawerThickness,gDrawerThickness);
	EndXtrd;
	ResetOrientation3D;
	Move3D(-1.414*gDrawerThickness/4+xoff,yoff,topOfDrawers-1*gDrawerThickness/2);
	Rotate3D(#90d 0' 0" ,#45d 0' 0" ,#0d 0' 0" );
END;
```
```python
SetAttrsByClassOrParent( vs.LNewObj(), gObjHandle, gPaving_Class )
vs.ResetOrientation3D()
vs.Rotate3D( 90.0, 0.0, 0.0 )
#### end of sweep for paving.

vs.EndMXtrd()
SetAttrsByClassOrParent(vs.LNewObj(), gObjHandle, gCurb_Class)
vs.ResetOrientation3D()
vs.Rotate3D( 90.0, 0.0, 90.0 )
```

## Version
Availability: from All Versions

## Category
* [General Edit](../Categories/General%20Edit.md)
