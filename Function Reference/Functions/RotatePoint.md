# RotatePoint

## Description
Procedure RotatePoint rotates selected VectorWorks objects about the specified coordinate point.

```pascal
PROCEDURE RotatePoint(
				pX,pY         : REAL;
				rotationAngle : REAL);
```

```python
def vs.RotatePoint(p, rotationAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Point of rotation.|
|rotationAngle|REAL|Rotation angle.|

## Examples
#### VectorScript ####
```pascal
SetSelect(LNewObj);
RotatePoint(0,3,45d);
```
#### Python ####
```python

```

```pascal
IF pFill<>kFill1 THEN BEGIN
	SetFPat(hShape2,0);
	{SetFillFore(hShape2,red,green,blue);}
END;
RotatePoint(0,0,pAngle);
MoveTo(A*(-1/4"),0);
LineTo(A*(1/4"),0);
hShape3 := lNewObj;
TextJust(2);

BeginGroup;
	{ draw five star chair base }
	FOR j := 1 TO 5 DO BEGIN
		Poly( -gCon/2, 0, -gCon/2, gCon*13, gCon/2, gCon*13, gCon/2, 0 );
		RotatePoint(0, 0, 72);
	END;

	LineTo(A*(0.01667"),A*(3/32"));
	MoveTo(A*(-0.01667"),A*(-3/32"));
	LineTo(A*(-0.01667"),A*(3/32"));
END;
RotatePoint(0,0,90);
PlaceLabel(0, 0.18021"*A);
```
```python
vs.RotatePoint((0, 0), 1.0)
```

## Version
Availability: from MiniCAD6.0

## Category
* [General Edit](../Categories/General%20Edit.md)
