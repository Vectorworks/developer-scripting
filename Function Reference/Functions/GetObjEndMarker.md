# GetObjEndMarker

## Description
Gets all properties for an object's end marker. Return TRUE if operation was successful.

```pascal
FUNCTION GetObjEndMarker(
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
def vs.GetObjEndMarker(obj):
    return (BOOLEAN, style, angle, size, width, thicknessBasis, thickness, visibility)
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
ok := GetObjEndMarker (h, style, angle, size, width, thickBasis, thickness, visibility);
Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness, ' /  ', visibility);
END;

RUN(Example);
```
#### Python ####
```python
def Example()
	h = vs.FSActLayer()
	ok, style, angle, size, width, thickBasis, thickness, visibility = vs.GetObjEndMarker (h)
	vs.Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness, ' /  ', visibility)
Example()
```

```pascal
BEGIN
	BSB := GetObjBeginningMarker( objHand, gArrowStyleIndex, gArrowAngle, gArrowSize, gArrowWidth, gThicknessBasis, gArrowThickness, begArrow );
	BSB := GetObjEndMarker( objHand, gArrowStyleIndex, gArrowAngle, gArrowSize, gArrowWidth, gThicknessBasis, gArrowThickness, endArrow );
END;

END;
if IsMarkerByClass(h1) then SetMarkerByClass(h2) else BEGIN
	BSB := GetObjBeginningMarker(h1,style,angle,length,width,thicknessBasis,thickness,visibility);
	BSB := SetObjBeginningMarker(h2,style,angle,length,width,thicknessBasis,thickness,visibility);
	BSB := GetObjEndMarker(h1,style,angle,length,width,thicknessBasis,thickness,visibility);
	BSB := SetObjEndMarker(h2,style,angle,length,width,thicknessBasis,thickness,visibility);
END;

IF pluginH = NIL THEN
	OK := GetDefaultEndMarker (markerStyle, markerAngle, markerSize, markerWidth, markerThkBasis, markerThickness, markerVisibility)
ELSE
	OK := GetObjEndMarker (pluginH,markerStyle, markerAngle, markerSize, markerWidth, markerThkBasis, markerThickness, markerVisibility);
```
```python
import vs

# Gets all properties for an object's end marker.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, style, angle, size, width, thicknessBasis, thickness, visibility = vs.GetObjEndMarker(obj)
vs.Message('GetObjEndMarker returned: ' + str((ok, style, angle, size, width, thicknessBasis, thickness, visibility)))
```

## See Also
VS Functions:
[GetObjBeginningMarker](GetObjBeginningMarker.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
