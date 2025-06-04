# GetTextOrientation

## Description
Procedure GetTextOrientation returns the position and orientation attributes of the referenced text object.

```pascal
PROCEDURE GetTextOrientation(
				theText                     : HANDLE;
				VAR textOriginX,textOriginY : REAL;
				VAR textAng                 : REAL;
				VAR textIsMirrored          : BOOLEAN);
```

```python
def vs.GetTextOrientation(theText):
    return (textOrigin, textAng, textIsMirrored)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|textOrigin|REAL|Returns coordinates of text origin.|
|textAng|REAL|Returns rotation angle of text.|
|textIsMirrored|BOOLEAN|Returns mirror state of text.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
theText :HANDLE;
textOriginX, textOriginY, textAng :REAL;
textIsMirrored :BOOLEAN;
BEGIN
theText := FSActLayer;
GetTextOrientation(theText, textOriginX, textOriginY, textAng, textIsMirrored);
Locus(textOriginX, textOriginY);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	theText = vs.FSActLayer()
	textOriginPt, textAng, textIsMirrored = vs.GetTextOrientation ( theText )
	vs.Locus(textOriginPt[0], textOriginPt[1])

Example()
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
