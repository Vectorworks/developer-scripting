# SetClassEndMarker

## Description
Sets all properties for the named class's end marker. Return TRUE if operation was successful.

```pascal
FUNCTION SetClassEndMarker(
				name           : STRING;
				style          : LONGINT;
				angle          : INTEGER;
				size           : REAL;
				width          : REAL;
				thicknessBasis : INTEGER;
				thickness      : REAL): BOOLEAN;
```

```python
def vs.SetClassEndMarker(name, style, angle, size, width, thicknessBasis, thickness):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of the class.|
|style|LONGINT|The marker style. (see comments for details)|
|angle|INTEGER|The marker angle in degrees. (0 to 90)|
|size|REAL|The marker size in page inches.|
|width|REAL|The marker width in page inches.|
|thicknessBasis|INTEGER|The marker thickness basis. ( see comments for details)|
|thickness|REAL|The marker thickness.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
ok : BOOLEAN;
BEGIN
ok := SetClassEndMarker('None', 1280, 25, 0.125, 0.125, 0, 2);
END;

RUN(Example);
```
#### Python ####
```python

```

## See Also
VS Functions:
[SetClassBeginningMarker](SetClassBeginningMarker.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Classes](../Categories/Classes.md)
