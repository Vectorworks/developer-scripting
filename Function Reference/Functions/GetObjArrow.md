# GetObjArrow

## Description
_Use [ GetObjBeginningMarker](GetObjBeginningMarker.md) and/or [ GetObjEndMarker](GetObjEndMarker.md) instead._
Procedure GetObjArrow returns the arrow style parameters for the indicated object.

```pascal
PROCEDURE GetObjArrow(
				obj       : HANDLE;
				VAR style : INTEGER;
				VAR size  : REAL;
				VAR angle : INTEGER;
				VAR start : BOOLEAN;
				VAR end   : BOOLEAN);
```

```python
def vs.GetObjArrow(obj):
    return (style, size, angle, start, end)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The indicated object.|
|style|INTEGER|Returns arrow style.|
|size|REAL|Returns arrow size in inches measured in page space.|
|angle|INTEGER|Returns arrow angle (in degrees).|
|start|BOOLEAN|Returns whether the start point of the object has an arrow.|
|end|BOOLEAN|Returns whether the endpoint of the object has an arrow.|

## Remarks
OBSOLETE for VW2008: Use GetObjBeginningMarker and/or GetObjEndMarker instead.
Style indicates the index of the arrow style to be used.

Size is in page-inches. Legal values are 0.0 to 2.0.

Angle is in degrees.

## Examples
#### VectorScript ####
```pascal
PROCEDURE ShowObjArrowValues;
VAR
style :INTEGER;
size	 :REAL;
ang	 :INTEGER;
start :BOOLEAN;
endPt :BOOLEAN;
obj   :HANDLE;
BEGIN
obj := FSActLayer;
GetObjArrow(obj, style, size, ang, start, endPt);
Message(style, ' ', size, ' ', ang, ' ', start, ' ', endPt);
END;
RUN(ShowObjArrowValues);
```

## Version
GetObjArrow is obsolete as of VectorWorks13.0<P>


Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
