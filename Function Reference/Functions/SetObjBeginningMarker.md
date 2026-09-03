# SetObjBeginningMarker

## Description
Sets all properties of an object's beginning marker. Return TRUE if operation was successful.

```pascal
FUNCTION SetObjBeginningMarker(
				obj            : HANDLE;
				style          : LONGINT;
				angle          : INTEGER;
				size           : REAL;
				width          : REAL;
				thicknessBasis : INTEGER;
				thickness      : REAL;
				visibility     : BOOLEAN): BOOLEAN;
```

```python
def vs.SetObjBeginningMarker(obj, style, angle, size, width, thicknessBasis, thickness, visibility):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|style|LONGINT|The marker style. (see comments for details)|
|angle|INTEGER|The marker angle in degrees. (0 to 90)|
|size|REAL|The marker size in page inches.|
|width|REAL|The marker width in page inches.|
|thicknessBasis|INTEGER|The marker thickness basis. ( see comments for details)|
|thickness|REAL|The marker thickness.|
|visibility|BOOLEAN|The marker visibility.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
ok : BOOLEAN;

BEGIN
MoveTo (0,0);
LineTo (100, 0);
ok := SetObjBeginningMarker(LNewObj, 1280, 25, 0.25, 0.125, 34, 2, TRUE);	
END;

RUN(Example);
```
#### Python ####
```python

```

```pascal
	anno:=Concat(GetPlugInString(3003),gNoTread+1,GetPlugInString(3004));
END;
Arc(-rad,-rad,rad,rad,90-angle,angle);
{SetArrow(LNewObj, 0, .1, 30, (pArrows=kCSStrDown), (pArrows <> kCSStrDown));}
BSB := SetObjBeginningMarker(LNewObj,0,30,.1,0,2,2,(pArrows=kCSStrDown));
BSB := SetObjEndMarker(LNewObj,0,30,.1,0,2,2,(pArrows <> kCSStrDown));
SetFPat(LNewObj,0);
angle:=angle*PI/(2*180);
Moveto(Sin(angle)*rad,cos(angle)*rad);

		END;
	begArrow := ((pArrows = 'Start') | (pArrows = 'Both'));
	endArrow := ((pArrows = 'End')   | (pArrows = 'Both'));
	{SetArrow(h1, arrowIndex, pArrow_Size / GetPrefReal(152), pArrow_Angle, begArrow, endArrow);}
	BSB := SetObjBeginningMarker(h1,arrowIndex,pArrow_Angle,pArrow_Size / GetPrefReal(152),Width,thicknessBasis,thickness,begArrow);
	BSB := SetObjEndMarker(h1,arrowIndex,pArrow_Angle,pArrow_Size / GetPrefReal(152),Width,thicknessBasis,thickness,endArrow);
END;

BEGIN
	MoveTo( startPoint.x, startPoint.y );
	LineTo( endPoint.x, endPoint.y );
	BSB := SetObjBeginningMarker( LNewObj, gArrowStyleIndex, gArrowAngle, gArrowSize, gArrowWidth, gThicknessBasis, gArrowThickness, begArrow );
	BSB := SetObjEndMarker( LNewObj, gArrowStyleIndex, gArrowAngle, gArrowSize, gArrowWidth, gThicknessBasis, gArrowThickness, endArrow );
	pt3 := ( startPoint + endPoint ) / 2;
END ELSE
BEGIN
```
```python
result = vs.SetObjBeginningMarker(obj, style, 1.0, 2.0, 0.5, 1.0, 2.0, True)
```

## See Also
VS Functions:
[SetObjEndMarker](SetObjEndMarker.md)

## Version
Availability: from VectorWorks 13.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
