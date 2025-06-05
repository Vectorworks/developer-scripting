# SetObjArrow

## Description
Procedure SetObjArrow sets the arrow style parameters for the indicated object.

**Marker Styles**

| Marker Style    | Constant |
|-----------------|----------|
| Filled Arrow    | 0        |
| Empty Arrow     | 1        |
| Open Arrow      | 2        |
| Filled Circle   | 3        |
| Empty Circle    | 4        |
| Slash           | 5        |
| Cross           | 6        |

```pascal
PROCEDURE SetObjArrow(
				obj   : HANDLE;
				style : INTEGER;
				size  : REAL;
				angle : INTEGER;
				start : BOOLEAN;
				end   : BOOLEAN);
```

```python
def vs.SetObjArrow(obj, style, size, angle, start, end):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The indicated object.|
|style|INTEGER|The arrow style.|
|size|REAL|The arrow size in inches measured in page space.|
|angle|INTEGER|The arrow angle (in degrees).|
|start|BOOLEAN|Whether the start point of the object has an arrow.|
|end|BOOLEAN|Whether the endpoint of the object has an arrow.|

## Remarks
OBSOLETE for VW2008: Use SetObjBeginningMarker and/or SetObjEndMarker instead.
Style indicates the index of the arrow style to be used.

Size is in page-inches. Legal values are 0.0 to 2.0.

Angle is in degrees.

## Examples
#### VectorScript ####
```pascal
PROCEDURE SetObjArrowValues;
BEGIN
SetObjArrow(FSActLayer, 1, .25, 15, TRUE, TRUE);
END;
RUN(SetObjArrowValues);
```
#### Python ####
```python

```

## Version
SetObjArrow is obsolete as of VectorWorks13.0<P>


Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
