# GetObjBeginningMarker

## Description
Gets all properties for an object's beginning marker. Return TRUE if operation was successful.

```pascal
FUNCTION GetObjBeginningMarker(
				obj                : HANDLE;
				VAR style          : LONGINT;
				VAR angle          : INTEGER;
				VAR size           : REAL;
				VAR width          : REAL;
				VAR thicknessBasis : INTEGER;
				VAR thickness      : REAL;
				VAR visibility     : BOOLEAN): BOOLEAN;
```

```python
def vs.GetObjBeginningMarker(obj):
    return (BOOLEAN, style, angle, size, width, thicknessBasis, thickness, visibility)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|style|LONGINT|The marker style. (see comments for details)|
|angle|INTEGER|The marker angle in degrees. (0 to 90)|
|size|REAL|The marker size in inches.|
|width|REAL|The marker width in inches.|
|thicknessBasis|INTEGER|The marker thickness basis. ( see comments for details)|
|thickness|REAL|The marker thickness.|
|visibility|BOOLEAN|The marker visibility.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h: HANDLE;
style: INTEGER;
angle: INTEGER;
size: REAL;
width: REAL;
thickBasis: INTEGER;
thickness: REAL;
visibility: BOOLEAN;

ok : BOOLEAN;

BEGIN
h := FSActLayer;
ok := GetObjBeginningMarker (h, style, angle, size, width, thickBasis, thickness, visibility);
Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness, ' /  ', visibility);
END;

RUN(Example);
```
#### Python ####
```python
def Example():
	h = vs.FSActLayer()
	ok, style, angle, size, width, thickBasis, thickness, visibility = vs.GetObjBeginningMarker (h)
	vs.Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness, ' /  ', visibility)

Example()
```

```pascal
BEGIN
	BSB := GetObjBeginningMarker( objHand, gArrowStyleIndex, gArrowAngle, gArrowSize, gArrowWidth, gThicknessBasis, gArrowThickness, begArrow );
	BSB := GetObjEndMarker( objHand, gArrowStyleIndex, gArrowAngle, gArrowSize, gArrowWidth, gThicknessBasis, gArrowThickness, endArrow );
END;

	GetPenBack(h1, r, g, b); SetPenBack(h2, r, g, b);
	GetPenFore(h1, r, g, b); SetPenFore(h2, r, g, b);
END;
if IsMarkerByClass(h1) then SetMarkerByClass(h2) else BEGIN
	BSB := GetObjBeginningMarker(h1,style,angle,length,width,thicknessBasis,thickness,visibility);
	BSB := SetObjBeginningMarker(h2,style,angle,length,width,thicknessBasis,thickness,visibility);
	BSB := GetObjEndMarker(h1,style,angle,length,width,thicknessBasis,thickness,visibility);
	BSB := SetObjEndMarker(h2,style,angle,length,width,thicknessBasis,thickness,visibility);
END;
```
```python
import vs

# Gets all properties for an object's beginning marker.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, style, angle, size, width, thicknessBasis, thickness, visibility = vs.GetObjBeginningMarker(obj)
vs.Message('GetObjBeginningMarker returned: ' + str((ok, style, angle, size, width, thicknessBasis, thickness, visibility)))
```

## See Also
VS Functions:
[GetObjEndMarker](GetObjEndMarker.md)

## Version
Availability: from VectorWorks 13.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
