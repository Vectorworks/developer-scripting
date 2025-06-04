# GetClassEndMarker

## Description
Gets all properties for the named class's end marker. Return TRUE if operation was successful.

```pascal
FUNCTION GetClassEndMarker(
				name               : STRING;
				VAR style          : LONGINT;
				VAR angle          : INTEGER;
				VAR size           : REAL;
				VAR width          : REAL;
				VAR thicknessBasis : INTEGER;
				VAR thickness      : REAL): BOOLEAN;
```

```python
def vs.GetClassEndMarker(name):
    return (BOOLEAN, style, angle, size, width, thicknessBasis, thickness)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of the class|
|style|LONGINT|The marker style (see comments for details)|
|angle|INTEGER|The marker angle in degrees (0 to 90)|
|size|REAL|The marker size in pages inches|
|width|REAL|The marker width in page inches|
|thicknessBasis|INTEGER|The marker thickness basis. ( see comments for details)|
|thickness|REAL|The marker thickness|

## Examples
#### VectorScript ####
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

BEGIN
ok := GetClassEndMarker('None', style, angle, size, width, thickBasis, thickness);	
Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness);	

END;

RUN(Example);
```
#### Python ####
```python
def Example():
	ok, style, angle, size, width, thickBasis, thickness = vs.GetClassEndMarker('None')
	vs.Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness)
Example()
```

## Version
Availability: from VectorWorks13.0

## Category
* [Classes](../Categories/Classes.md)
