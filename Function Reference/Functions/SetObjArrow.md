# SetObjArrow

## Description
Procedure SetObjArrow sets the arrow style parameters for the indicated object.

**Marker Styles**

| Marker Style    | Constant |
|-----------------|----------|
| Filled Arrow    | 0        |
| Empty Arrow     | 1        |
| Open Arrow      | 2        |
| Filled Circle   | 3        |
| Empty Circle    | 4        |
| Slash           | 5        |
| Cross           | 6        |

```pascal
PROCEDURE SetObjArrow(
				obj   : HANDLE;
				style : INTEGER;
				size  : REAL;
				angle : INTEGER;
				start : BOOLEAN;
				end   : BOOLEAN);
```

```python
def vs.SetObjArrow(obj, style, size, angle, start, end):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The indicated object.|
|style|INTEGER|The arrow style.|
|size|REAL|The arrow size in inches measured in page space.|
|angle|INTEGER|The arrow angle (in degrees).|
|start|BOOLEAN|Whether the start point of the object has an arrow.|
|end|BOOLEAN|Whether the endpoint of the object has an arrow.|

## Remarks
OBSOLETE for VW2008: Use SetObjBeginningMarker and/or SetObjEndMarker instead.
Style indicates the index of the arrow style to be used.

Size is in page-inches. Legal values are 0.0 to 2.0.

Angle is in degrees.

## Examples
#### VectorScript ####
```pascal
PROCEDURE SetObjArrowValues;
BEGIN
SetObjArrow(FSActLayer, 1, .25, 15, TRUE, TRUE);
END;
RUN(SetObjArrowValues);
```
#### Python ####
```python

```

```pascal
Lin(begWit, endWit); SetPenFore(LNewObj, 65535, 0, 0);
begWit := begPt + (Perp(tmpUnitVec) * 12");
endWit := endPt + (Perp(tmpUnitVec) * 12");
Lin(begWit, endWit); SetPenFore(LNewObj, 65535, 0, 0);
SetObjArrow(LNewObj, 0, .125, 25, TRUE, TRUE);
CreateText(text);

MoveTo( 0, 0 );
LineTo( ControlPoint_01.x, ControlPoint_01.y );
SetPenFore(LNewObj, 65535, 0, 0);
IF pInteriorCorner
	THEN SetObjArrow( LNewObj, 0, 0.15, 15, TRUE, FALSE )
	ELSE SetObjArrow( LNewObj, 0, 0.15, 15, FALSE, TRUE );

MoveTo(vDimLineStart.x,vDimLineStart.y);
LineTo(vDimLineEnd.x,vDimLineEnd.y);
SetObjArrow (LNewObj,0,(P__ArrowSize/upi),13,TRUE,TRUE);
```
```python
vs.SetObjArrow(obj, style, 1.0, 2.0, start, end)
```

## Version
SetObjArrow is obsolete as of VectorWorks13.0<P>

Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
