# GetMarker

## Description
<b>OBSOLETE for VW2008: Use [[VS:GetObjBeginningMarker| GetObjBeginningMarker]] and/or [[VS:GetObjEndMarker| GetObjEndMarker]] instead.</b>
Returns marker information on the referenced object.

```pascal
PROCEDURE GetMarker(
				h         : HANDLE;
				VAR start : BOOLEAN;
				VAR end   : BOOLEAN;
				VAR style : INTEGER;
				VAR size  : REAL);
```

```python
def vs.GetMarker(h):
    return (start, end, style, size)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the object.|
|start|BOOLEAN|True if a marker is visible at start of object.|
|end|BOOLEAN|True if a marker is visible at end of object.|
|style|INTEGER|Marker style:|0 - Filled Arrow Marker|1 - Empty Arrow Marker|2 - Open Arrow Marker|3 - Filled Ball Marker|4 - Empty Ball Marker|5 - Slash Marker|6 - Cross Marker|
|size|REAL|Size of marker.|

## Remarks
OBSOLETE for VW2008: Use [[VS:GetObjBeginningMarker| GetObjBeginningMarker]] and/or [[VS:GetObjEndMarker| GetObjEndMarker]] instead.
For a one inch marker pass in a size value equal to 16384. If you pass NIL for the obj parameter, this call will set the marker defaults for this document.  angle must be in range 0 to 90 degrees.

## Examples
#### VectorScript ####
```pascal
PROCEDURE CheckMarker;
VAR
h: HANDLE;
MarkerStyle: INTEGER;
StartMark, EndMark: BOOLEAN;
Size: REAL;
BEGIN
h := FSActLayer;
GetMarker(H, StartMark, EndMark, MarkerStyle, Size);
Message('StartMark: ', StartMark, ' EndMark:', EndMark, ' MarkerStyle:', MarkerStyle, ' Size:', Size);
END;
RUN(CheckMarker);
```
#### Python ####
```python
def CheckMarker():
	h = vs.FSActLayer()
	StartMark, EndMark, MarkerStyle, Size = vs.GetMarker(h)
	vs.Message('StartMark: ', StartMark, ' EndMark:', EndMark, ' MarkerStyle:', MarkerStyle, ' Size:', Size)

CheckMarker()
```

## See Also
VS Functions:
* [SetMarker](SetMarker.md)
* [GetObjBeginningMarker| GetObjBeginningMarker](GetObjBeginningMarker|%20GetObjBeginningMarker.md)
* [GetObjEndMarker| GetObjEndMarker](GetObjEndMarker|%20GetObjEndMarker.md)

## Version
GetMarker is obsolete as of VectorWorks 13.0

Availability: from VectorWorks 10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
