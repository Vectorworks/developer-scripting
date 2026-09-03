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

```pascal
BEGIN
	IF GetClassEndMarker(GetClass(LNewObj), style, angle, size, width, thicknessBasis, thickness) THEN
	BEGIN
		{Trick here.}
		{You have to use SetObjEndMarker to turn the marker ON then you can reset it to ByClass and the MarkerVisibility sticks}
		OK := SetObjEndMarker (LNewObj, style, angle, size, width, thicknessBasis, thickness, gMarkerVisibility);
		SetMarkerByClass(lNewObj);
		OK := SetObjEndMarker (pluginH, style, angle, size, width, thicknessBasis, thickness, gMarkerVisibility);
		SetMarkerByClass(pluginH);
	END;

thickBasis := 0;
thick := 0;
ok := SetObjEndMarker(ptrLine,style,ang,size,wid,thickBasis,thick,TRUE);
SetClass(ptrLine,pointerClass);
ok := GetClassEndMarker(pointerClass,style,ang,size,wid,thickBasis,thick);
IF NOT ok THEN
	BEGIN
		style := 0;
		ang := 15;
```
```python
import vs

# Gets all properties for the named class's end marker.
name = 'Example'

ok, style, angle, size, width, thicknessBasis, thickness = vs.GetClassEndMarker(name)
vs.Message('GetClassEndMarker returned: ' + str((ok, style, angle, size, width, thicknessBasis, thickness)))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Classes](../Categories/Classes.md)
