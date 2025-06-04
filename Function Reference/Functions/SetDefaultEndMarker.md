# SetDefaultEndMarker

## Description
Sets all properties of the document default end marker. Return TRUE if operation was successful.

```pascal
FUNCTION SetDefaultEndMarker(
				style          : LONGINT;
				angle          : INTEGER;
				size           : REAL;
				width          : REAL;
				thicknessBasis : INTEGER;
				thickness      : REAL;
				visibility     : BOOLEAN): BOOLEAN;
```

```python
def vs.SetDefaultEndMarker(style, angle, size, width, thicknessBasis, thickness, visibility):
    return BOOLEAN
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
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
ok : BOOLEAN;
BEGIN
ok := SetDefaultEndMarker(2176, 15, 0.5, 0, 0, 2, TRUE);	
END;

RUN(Example);
```
#### Python ####
```python

```

## See Also
VS Functions:
[SetDefaultBeginningMarker](SetDefaultBeginningMarker.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
