# Get3DCntr

## Description
Procedure Get3DCntr returns the three-dimensional center point of the referenced 3D object (BoundingBox).

```pascal
PROCEDURE Get3DCntr(
				h          : HANDLE;
				VAR pX,pY  : REAL;
				VAR zValue : REAL);
```

```python
def vs.Get3DCntr(h):
    return (p, zValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|p|REAL|Returns coordinates of object center point.|
|zValue|REAL|Returns elevation of object center point.|

## Examples

```pascal
VSWarnings := GetPref( 21 ); { save the settings about VS warnings before disabling them }
SetPref( 21, FALSE );
Get3DCntr(gPluginH, Xval, Yval, Zval);

BEGIN
	Get3DCntr(pluginH, xValue, yValue, zValue);
	Move3DObj(pluginH, (CenterX - xCurr), (CenterY - yCurr), - zValue);
END

While GetObject(Concat(GetPlugInString(7029),I)) <> NIL DO
	I := I+1;
SymName := Concat(GetPlugInString(7029),I);
IF GetObjectVariableBoolean(h,650) THEN
	Get3DCntr(h, xLoc, yLoc, zLoc)
ELSE
	HCenter(h, xLoc, yLoc);
SetSelect(h);
```
```python
import vs

# Procedure Get3DCntr returns the three-dimensional center point of the
# referenced 3D object (BoundingBox).
h = vs.FSActLayer()  # handle to the first selected object on the active layer

p, zValue = vs.Get3DCntr(h)
vs.Message('Get3DCntr returned: ' + str((p, zValue)))
```

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
