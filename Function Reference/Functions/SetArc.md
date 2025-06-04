# SetArc

## Description
Procedure SetArc sets the start and sweep angles of the referenced arc or round wall object.   Specify the angles in degrees.

```pascal
PROCEDURE SetArc(
				h          : HANDLE;
				startAngle : REAL;
				arcAngle   : REAL);
```

```python
def vs.SetArc(h, startAngle, arcAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to arc.|
|startAngle|REAL|New start angle of arc.|
|arcAngle|REAL|New sweep angle of arc.|

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

```

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
