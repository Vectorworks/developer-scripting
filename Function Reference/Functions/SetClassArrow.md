# SetClassArrow

## Description
Procedure SetClassArrow sets the arrow style parameters for the indicated class.

```pascal
PROCEDURE SetClassArrow(
				className : STRING;
				style     : INTEGER;
				size      : REAL;
				angle     : INTEGER);
```

```python
def vs.SetClassArrow(className, style, size, angle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|The indicated class.|
|style|INTEGER|The arrow style.|
|size|REAL|The arrow size in inches measured in page space.|
|angle|INTEGER|The arrow angle (in degrees).|

## Remarks
OBSOLETE for VW2008: Use SetClassBeginningMarker and/or SetClassEndMarker instead.
Style indicates the index of the arrow style to be used.

Size is in page-inches. Legal values are 0.0 to 2.0.

Angle is in degrees.

## Examples
==== VectorScript ====
```pascal
SetClassArrow('None', 2, 0.25, 15);
```
==== Python ====
```python

```

## Version
SetClassArrow is obsolete as of VectorWorks13.0<P>


Availability: from VectorWorks10.0

## Category
* [Classes](../Categories/Classes.md)
