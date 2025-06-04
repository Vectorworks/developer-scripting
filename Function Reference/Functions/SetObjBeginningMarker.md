# SetObjBeginningMarker

## Description
Sets all properties of an object's beginning marker. Return TRUE if operation was successful.

```pascal
FUNCTION SetObjBeginningMarker(
				obj            : HANDLE;
				style          : LONGINT;
				angle          : INTEGER;
				size           : REAL;
				width          : REAL;
				thicknessBasis : INTEGER;
				thickness      : REAL;
				visibility     : BOOLEAN): BOOLEAN;
```

```python
def vs.SetObjBeginningMarker(obj, style, angle, size, width, thicknessBasis, thickness, visibility):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|style|LONGINT|The marker style. (see comments for details)|
|angle|INTEGER|The marker angle in degrees. (0 to 90)|
|size|REAL|The marker size in page inches.|
|width|REAL|The marker width in page inches.|
|thicknessBasis|INTEGER|The marker thickness basis. ( see comments for details)|
|thickness|REAL|The marker thickness.|
|visibility|BOOLEAN|The marker visibility.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
ok : BOOLEAN;

BEGIN
MoveTo (0,0);
LineTo (100, 0);
ok := SetObjBeginningMarker(LNewObj, 1280, 25, 0.25, 0.125, 34, 2, TRUE);	
END;

RUN(Example);
```
#### Python ####
```python

```

## See Also
VS Functions:
[SetObjEndMarker](SetObjEndMarker.md)

## Version
Availability: from VectorWorks 13.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
