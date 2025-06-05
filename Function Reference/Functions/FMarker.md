# FMarker

## Description
_OBSOLETE for VW 2008: Use [ GetDefaultBeginningMarker](GetDefaultBeginningMarker.md) and/or [ GetDefaultEndMarker](GetDefaultEndMarker.md) instead._
Procedure FMarker returns the active marker style parameters.

A complete listing of marker styles can be found in the [Script Appendix](../Appendix/pages/Appendix%20I%20-%20Markers.md).

```pascal
PROCEDURE FMarker(
				VAR style : INTEGER;
				VAR size  : REAL;
				VAR ang   : INTEGER);
```

```python
def vs.FMarker():
    return (style, size, ang)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|style|INTEGER|Returns marker style.|
|size|REAL|Returns marker size in inches measured in page space.|
|ang|INTEGER|Returns marker angle (in degrees).|

## Remarks
OBSOLETE for VW 2008: Use [ GetDefaultBeginningMarker](GetDefaultBeginningMarker.md) and/or [ GetDefaultEndMarker](GetDefaultEndMarker.md) instead.
Style is an 8 bit quantity interpreted as follows:

* Bit 0 indicates the visibility of a marker at the start of the line.
* Bit 1 indicates the visibility of a marker at the end of the line.
* Bits 2 - 7 indicate the index of the marker style to be used.

Size is in page-inches. Legal values are 0.0 to 2.0.

Angle is in degrees.

The parameter Style is currently returning 0-6, 0 for solid arrow, 1 for empty arrow, etc. and not the 8 bit quantity as described above.

Actually, the Style is returning:
* 0 for solid arrow,
* 4 for empty arrow*
* 8 for open arrow
* 12 for dot, etc.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
style :INTEGER;
size  :REAL;
ang   :INTEGER;
BEGIN
FMarker(style, size, ang);
Message(style, ' ', size, ' ', ang);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	style, size, ang = vs.FMarker()
	vs.Message(style, ' ', size, ' ', ang)
Example()
```

## See Also
VS Functions:
* [GetDefaultBeginningMarker](GetDefaultBeginningMarker.md)
* [GetDefaultEndMarker](GetDefaultEndMarker.md)

## Version
FMarker is obsolete as of VectorWorks 13.0

Availability: from MiniCAD 6.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
