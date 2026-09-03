# GetObjArrow

## Description
_Use [ GetObjBeginningMarker](GetObjBeginningMarker.md) and/or [ GetObjEndMarker](GetObjEndMarker.md) instead._
Procedure GetObjArrow returns the arrow style parameters for the indicated object.

```pascal
PROCEDURE GetObjArrow(
				obj       : HANDLE;
				VAR style : INTEGER;
				VAR size  : REAL;
				VAR angle : INTEGER;
				VAR start : BOOLEAN;
				VAR end   : BOOLEAN);
```

```python
def vs.GetObjArrow(obj):
    return (style, size, angle, start, end)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The indicated object.|
|style|INTEGER|Returns arrow style.|
|size|REAL|Returns arrow size in inches measured in page space.|
|angle|INTEGER|Returns arrow angle (in degrees).|
|start|BOOLEAN|Returns whether the start point of the object has an arrow.|
|end|BOOLEAN|Returns whether the endpoint of the object has an arrow.|

## Remarks
OBSOLETE for VW2008: Use GetObjBeginningMarker and/or GetObjEndMarker instead.
Style indicates the index of the arrow style to be used.

Size is in page-inches. Legal values are 0.0 to 2.0.

Angle is in degrees.

## Examples
#### VectorScript ####
```pascal
PROCEDURE ShowObjArrowValues;
VAR
style :INTEGER;
size	 :REAL;
ang	 :INTEGER;
start :BOOLEAN;
endPt :BOOLEAN;
obj   :HANDLE;
BEGIN
obj := FSActLayer;
GetObjArrow(obj, style, size, ang, start, endPt);
Message(style, ' ', size, ' ', ang, ' ', start, ' ', endPt);
END;
RUN(ShowObjArrowValues);
```

```pascal
	tempV := UnitVec( Ang2Vec( ang , 1) ) * GetTextWidth( textH )/2 + originVec;
	originVec := UnitVec( Ang2Vec( ang + 180 , 1) ) * GetTextWidth( textH )/2 + originVec;
END;
if arcLineH <> nil then BEGIN
	GetObjArrow( arcLineH, style, size, Angle, bstart, bend );
	if bstart then GetSegPt1( arcLineH, vec1[1], vec1[2] ) ELSE GetSegPt2( arcLineH, vec1[1], vec1[2] );
end else BEGIN
	GetObjArrow( arrowLineH, style, size, Angle, bstart, bend );
	if bstart then GetSegPt2( arrowLineH, vec1[1], vec1[2] ) ELSE GetSegPt1( arrowLineH, vec1[1], vec1[2] );
```
```python
import vs

# _ Procedure GetObjArrow returns the arrow style parameters for the
# indicated object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

style, size, angle, start, end = vs.GetObjArrow(obj)
vs.Message('GetObjArrow returned: ' + str((style, size, angle, start, end)))
```

## Version
GetObjArrow is obsolete as of VectorWorks13.0<P>

Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
