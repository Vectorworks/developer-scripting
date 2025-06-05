# GetClassArrow

## Description
Procedure GetClassArrow returns the arrow style parameters for the indicated class.

```pascal
PROCEDURE GetClassArrow(
				className : STRING;
				VAR style : INTEGER;
				VAR size  : REAL;
				VAR angle : INTEGER);
```

```python
def vs.GetClassArrow(className):
    return (style, size, angle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|The indicated class.|
|style|INTEGER|Returns arrow style.|
|size|REAL|Returns arrow size in inches measured in page space.|
|angle|INTEGER|Returns arrow angle (in degrees).|

## Remarks
OBSOLETE for VW2008: Use [ GetClassBeginningMarker](GetClassBeginningMarker.md) and/or [ GetClassEndMarker](GetClassEndMarker.md) instead.
Style indicates the index of the arrow style to be used.

Size is in page-inches. Legal values are 0.0 to 2.0.

Angle is in degrees.

## Examples
#### VectorScript ####
```pascal
PROCEDURE ShowNoneClassArrowValues;
VAR
style :INTEGER;
size  :REAL;
ang   :INTEGER;
BEGIN
GetClassArrow('None', style, size, ang);
Message(style, ' ', size, ' ', ang);
END;
RUN(ShowNoneClassArrowValues);
```
#### Python ####
```python

```

## See Also
VS Functions:
* [GetClassBeginningMarker](GetClassBeginningMarker.md)
* [GetClassEndMarker](GetClassEndMarker.md)

## Version
GetClassArrow is obsolete as of VectorWorks 13.0

Availability: from VectorWorks 10.0

## Category
* [Classes](../Categories/Classes.md)
