# SetSegPt1

## Description
Procedure SetSegPt1 sets the location of the start point of the referenced line or wall object.

```pascal
PROCEDURE SetSegPt1(
				h     : HANDLE;
				pX,pY : REAL);
```

```python
def vs.SetSegPt1(h, p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to line.|
|p|REAL|New start point of line.|

## Remarks
Although GetSegPt1 works on linear dimensions this call does not successfully set the pt for a dimension.

## Examples
#### VectorScript ####
```pascal
PROCEDURE ExtendLine;
CONST
kEXTENSION = 250mm;

PROCEDURE ProcessLine(lineHdl :HANDLE);
VAR
size :REAL;
lineVec :VECTOR;
arrow1,arrow2 :BOOLEAN;
style,angle :INTEGER;
p1X,p1Y,p2X,p2Y,lineLen :REAL;
BEGIN
GetSegPt1(lineHdl, p1X, p1Y);
GetSegPt2(lineHdl, p2X, p2Y);
GetObjArrow(lineHdl, style, size, angle, arrow1, arrow2);
IF arrow1 THEN BEGIN
lineVec[1] := p1X - p2X;
lineVec[2] := p1Y - p2Y;
lineLen := Norm(lineVec);
lineVec := (lineLen + kEXTENSION) * UnitVec(lineVec);
p1X := p2X + lineVec[1];
p1Y := p2Y + lineVec[2];
SetSegPt1(lineHdl, p1X, p1Y);
END ELSE BEGIN
lineVec[1] := p2X - p1X;
lineVec[2] := p2Y - p1Y;
lineLen := Norm(lineVec);
lineVec := (lineLen + kEXTENSION) * UnitVec(lineVec);
p2X := p1X + lineVec[1];
p2Y := p1Y + lineVec[2];
SetSegPt2(lineHdl, p2X, p2Y);
END;
END;

BEGIN
ForEachObject(ProcessLine, (((C='LineClass') &amp; (T=LINE))));
END;
RUN(ExtendLine);
```
#### Python ####
```python

```

## See Also
VS Functions:
[SetSegPt2](SetSegPt2.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
