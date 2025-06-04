# SetMarker

## Description
Specifies marker information for the referenced object - OBSOLETE procedure: Use SetObjBeginningMarker and/or SetObjEndMarker instead.

```pascal
PROCEDURE SetMarker(
				h     : HANDLE;
				start : BOOLEAN;
				end   : BOOLEAN;
				style : INTEGER;
				size  : REAL);
```

```python
def vs.SetMarker(h, start, end, style, size):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the object|
|start|BOOLEAN|True if a marker is visible at start of object.|
|end|BOOLEAN|True if a marker is visible at end of object.|
|style|INTEGER|Marker style:|0 - Filled Arrow Marker|1 - Empty Arrow Marker|2 - Open Arrow Marker|3 - Filled Ball Marker|4 - Empty Ball Marker|5 - Slash Marker|6 - Cross Marker|
|size|REAL|Size of marker|

## Remarks
OBSOLETE for VW2008: Use SetObjBeginningMarker and/or SetObjEndMarker instead.


This changes the document defaults.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
BEGIN
MoveTo(0, 0);
LineTo(100, 0);
SetMarker(LNewObj, TRUE, FALSE, 2, 10000);
END;
RUN(Example);
```
==== Python ====
```python

```

## See Also
VS Functions:
[GetMarker](GetMarker.md) 
| [SetObjBeginningMarker](SetObjBeginningMarker.md) 
| [SetObjEndMarker](SetObjEndMarker.md)

## Version
SetMarker is obsolete as of VectorWorks13.0<P>


Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
