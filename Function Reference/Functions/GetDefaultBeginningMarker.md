# GetDefaultBeginningMarker

## Description
Gets all properties for the document default beginning marker. Return TRUE if operation was successful.

```pascal
FUNCTION GetDefaultBeginningMarker(
				VAR style          : LONGINT;
				VAR angle          : INTEGER;
				VAR size           : REAL;
				VAR width          : REAL;
				VAR thicknessBasis : INTEGER;
				VAR thickness      : REAL;
				VAR visibility     : BOOLEAN): BOOLEAN;
```

```python
def vs.GetDefaultBeginningMarker():
    return (BOOLEAN, style, angle, size, width, thicknessBasis, thickness, visibility)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|style|LONGINT|The marker style. (see comments for details)|
|angle|INTEGER|The marker angle in degrees. (0 to 90)|
|size|REAL|The marker size in page inches.|
|width|REAL|The marker width in page inches.|
|thicknessBasis|INTEGER|The marker thickness basis. ( see comments for details)|
|thickness|REAL|The marker thickness.|
|visibility|BOOLEAN|The marker visibility.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
ok : BOOLEAN;
style: INTEGER;
angle: INTEGER;
size: REAL;
width: REAL;
thickBasis: INTEGER;
thickness: REAL;
visibility: BOOLEAN;


BEGIN
ok := GetDefaultBeginningMarker (style, angle, size, width, thickBasis, thickness, visibility);
Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness, ' /  ', visibility);	
END;

RUN(Example);
```
==== Python ====
```python
def Example():
	ok, style, angle, size, width, thickBasis, thickness, visibility = vs.GetDefaultBeginningMarker ()
	vs.Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness, ' /  ', visibility)
Example()
```

## See Also
VS Functions:
[GetDefaultEndMarker](GetDefaultEndMarker.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
