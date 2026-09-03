# Marker

## Description
_OBSOLETE for VW2008: Use [SetDefaultBeginningMarker](SetDefaultBeginningMarker.md) and/or [SetDefaultEndMarker](SetDefaultEndMarker.md) instead._
Marker defines a marker (arrowhead) style for the document. This marker style becomes the active style for the document.

A complete listing of marker styles can be found in the [Script Appendix](../Appendix/pages/Appendix%20I%20-%20Markers.md).

```pascal
PROCEDURE Marker(
				style : INTEGER;
				size  : REAL;
				ang   : INTEGER);
```

```python
def vs.Marker(style, size, ang):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|style|INTEGER|Marker style constant.|
|size|REAL|Marker size in inches measured in page space.  Legal values are 0.0 to 2.0.|
|ang|INTEGER|Marker angle.|

## Remarks
OBSOLETE for VW2008: Use SetDefaultBeginningMarker and/or SetDefaultEndMarker instead.
See FMarker for parameter descriptions.

[sd 8/14/98]

## Examples
#### VectorScript ####
```pascal
Marker(2,0.25,60);
```
#### Python ####
```python

```

```pascal
EndXtrd;
ResetOrientation3D;
Rotate3D(#90.0,#0.0,#90.0);
Move3D(0e0',0e0',0e0');
Marker(0,0.125,15);
MoveTo(-7.1875e-1',-1.333e0');
LineTo(-7.1875e-1',-1.041667e-1');
MoveTo(7.1875e-1',-1.3333e0');
LineTo(7.1875e-1',-1.041667e-1');

Marker(0,0,0);

Marker(0,0,0);
SetScaleFactor;
SetFixFactor;
```
```python
if ok and ResourceIsOK():
	vs.PushAttrs()
	vs.Marker( 0, 0, 0 )
	if objectHand != None:
		noneClass = vs.GetClass( objectHand )
		succeeded = True

prefInt3DRes = vs.GetPrefInt( 56 )
vs.SetPrefInt( 5556, kPrefInt3DRes )
vs.Marker( 0, 0, 0 )
vs.ClosePoly()
```

## Version
Marker is obsolete as of VectorWorks13.0<P>

Availability: from MiniCAD6.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
