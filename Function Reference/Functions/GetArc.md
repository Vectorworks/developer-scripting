# GetArc

## Description
Procedure GetArc returns the start and sweep angle of the referenced arc or round wall.

```pascal
PROCEDURE GetArc(
				h               : HANDLE;
				VAR startAngleR : REAL;
				VAR arcAngleR   : REAL);
```

```python
def vs.GetArc(h):
    return (startAngleR, arcAngleR)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to arc.|
|startAngleR|REAL|Returns start angle of arc.|
|arcAngleR|REAL|Returns sweep angle of arc.|

## Remarks
On round walls, this call won't detect if the wall is reversed or not (should return the inverse of the angle, if the wall is reversed).

## Examples
#### VectorScript ####
```pascal
PROCEDURE GetArcSetArcExample;
VAR
h :HANDLE;
startAng, sweepAng :REAL;
BEGIN
h := FSActLayer;
GetArc(h, startAng, sweepAng);
SetArc(h, startAng, sweepAng + 10);
END;
RUN(GetArcSetArcExample);
```
#### Python ####
```python
def GetArcSetArcExample():
	h = vs.FSActLayer()
	if h != None:
		startAng, sweepAng = vs.GetArc(h)
		vs.SetArc(h, startAng, sweepAng + 10)
GetArcSetArcExample()
```

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
