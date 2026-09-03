# CC_RouteFromShape

## Description
Creates cable route from the given shape. The shape must be polygon, polyline or 3D polygon.

```pascal
PROCEDURE CC_RouteFromShape(hObj : HANDLE);
```

```python
def vs.CC_RouteFromShape(hObj):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|   |

## Examples
```pascal
BEGIN
	IF h3DPoly <> NIL THEN gPluginObjH := CC_RouteFromShape(h3DPoly)
	ELSE gPluginObjH := CC_RouteFromShape(h);
END;	{of MakeCableRoute}
```
```python
import vs

# Creates cable route from the given shape.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.CC_RouteFromShape(hObj)
```

## Version
Availability: from Vectorworks 2022

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
