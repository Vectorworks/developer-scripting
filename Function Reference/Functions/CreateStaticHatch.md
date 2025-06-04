# CreateStaticHatch

## Description
Creates a static hatch using inHatchName inside the bounded selection surrounding the point. rotationAngle determines the rotation of the result.

```pascal
FUNCTION CreateStaticHatch(
				inHatchName   : STRING;
				pX,pY         : REAL;
				rotationAngle : REAL): HANDLE;
```

```python
def vs.CreateStaticHatch(inHatchName, p, rotationAngle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inHatchName|STRING|The name of the hatch definition to use for the hatch.|
|p|REAL|A point inside the bounds defined by the current selection|
|rotationAngle|REAL|An angle that specifies an offset angle.  Zero degress is due East.|

## Remarks
The hatch is created in an arbitrary angle, not as defined.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h:HANDLE;
x,y:REAL;
BEGIN
GetPt(x,y);
h := CreateStaticHatch('Default Hatch', x, y, 0);
DSelectAll;
SetSelect(h);
END;
RUN(Example);
```
==== Python ====
```python
def PickPointCallback(pt):
	h = vs.CreateStaticHatch('Default Hatch', pt[0], pt[1], 0)
	vs.DSelectAll()
	vs.SetSelect(h)

vs.GetPt( PickPointCallback )
```

## Version
Availability: from VectorWorks10.1

## Category
* [Hatches @ Vector Fills](../Categories/Hatches%20-%20Vector%20Fills.md)
