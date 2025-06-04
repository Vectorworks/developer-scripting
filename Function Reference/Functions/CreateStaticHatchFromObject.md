# CreateStaticHatchFromObject

## Description
Creates a static hatch using inHatchName inside the bounds of the inObj.  The pX , pY and rotationAngle arguments determine the hatch origin and rotation used to generate the result.

```pascal
FUNCTION CreateStaticHatchFromObject(
				inObj         : HANDLE;
				inHatchName   : STRING;
				pX,pY         : REAL;
				rotationAngle : REAL): HANDLE;
```

```python
def vs.CreateStaticHatchFromObject(inObj, inHatchName, p, rotationAngle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inObj|HANDLE|An object used as the boundary for the output.|
|inHatchName|STRING|The name of the hatch definition|
|p|REAL|A point specifying the origin of the output|
|rotationAngle|REAL|An angle specifying an offset angle to use to create the output|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h:HANDLE;
x,y:REAL;
BEGIN
GetPt(x,y);
h := CreateStaticHatchFromObject(FSActLayer,'Default Hatch', x, y, 0);
DSelectAll;
SetSelect(h);
END;
RUN(Example);
```
==== Python ====
```python
def PickPointCallback(pt):
	h = vs.CreateStaticHatchFromObject(vs.FSActLayer(),'Default Hatch', pt[0], pt[1], 0)
vs.GetPt( PickPointCallback )
```

## Version
Availability: from VectorWorks10.5

## Category
* [Hatches @ Vector Fills](../Categories/Hatches%20-%20Vector%20Fills.md)
