# GetPointAndParameterOnNurbsCurveAtGivenLength

## Description
Gets point, parametric parameter, and curve index of specified location along a NURBS Curve.

```pascal
FUNCTION GetPointAndParameterOnNurbsCurveAtGivenLength(
				inNurbCurve       : HANDLE;
				inPercentOfLength : REAL;
				VAR pX,pY,pZ      : REAL;
				VAR outParam      : REAL;
				VAR outIndex      : LONGINT): BOOLEAN;
```

```python
def vs.GetPointAndParameterOnNurbsCurveAtGivenLength(inNurbCurve, inPercentOfLength):
    return (BOOLEAN, p, outParam, outIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inNurbCurve|HANDLE|Handle to the NURBS curve.|
|inPercentOfLength|REAL|Specify location on curve as percent of total length.  (0 - 1)|
|p|REAL|Point of specified location.|
|outParam|REAL|Parametric parameter of location.|
|outIndex|LONGINT|0-based index of piece for piecewise NURBS curve.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
inNurbCurve :HANDLE;
inPercentOfLength :REAL;
pX, pY, pZ :REAL;
outParam :REAL;
outIndex :LONGINT;
BEGIN
CallTool(-325);
inNurbCurve := FSActLayer;
inPercentOfLength := .5;
IF GetPointAndParameter(inNurbCurve, inPercentOfLength, pX, pY, pZ, outParam, outIndex) THEN BEGIN
Locus3D(pX, pY, pZ);
END;
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	vs.CallTool(-325)
	inNurbCurve = vs.FSActLayer()
	inPercentOfLength = 0.5
	isNurbss, outPt, outParam, outIndex = vs.GetPointAndParameter(inNurbCurve, inPercentOfLength)
	if isNurbss:
		vs.Locus3D(outPt[0], outPt[1], outPt[2])

Example()
```

```pascal
nurbs[1].x := pX;
nurbs[1].y := pY;
nurbs[1].z := pZ;
for cnt := 2 to nurbsPtCnt - 1 do BEGIN
	if GetPointAndParameterOnNurbsCurveAtGivenLength(nurbsHandle, (gStationSpacing * (cnt-1)) / nurbsLength, pX, pY, pZ, outParam, outIndex) then BEGIN
		nurbs[cnt].x := pX;
		nurbs[cnt].y := pY;
		nurbs[cnt].z := pZ;
	END ELSE nurbsPtCnt := nurbsPtCnt - 1;
END;
```
```python
import vs

# Gets point, parametric parameter, and curve index of specified location
# along a NURBS Curve.
inNurbCurve = vs.FSActLayer()  # handle to the first selected object on the active layer
inPercentOfLength = 1.0

ok, p, outParam, outIndex = vs.GetPointAndParameterOnNurbsCurveAtGivenLength(inNurbCurve, inPercentOfLength)
vs.Message('GetPointAndParameterOnNurbsCurveAtGivenLength returned: ' + str((ok, p, outParam, outIndex)))
```

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
