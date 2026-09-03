# Set3DInfo

## Description
Procedure Set3DInfo sets the height, width and depth dimensions of the referenced object.

```pascal
PROCEDURE Set3DInfo(
				h              : HANDLE;
				heightDistance : REAL;
				widthDistance  : REAL;
				depthDistance  : REAL);
```

```python
def vs.Set3DInfo(h, heightDistance, widthDistance, depthDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to 3D object.|
|heightDistance|REAL|New height of object.|
|widthDistance|REAL|New width of object.|
|depthDistance|REAL|New depth of object.|

## Examples
```pascal
Set3DInfo(h, 1.0, 2.0, 0.5);
```
```python
import vs

# Procedure Set3DInfo sets the height, width and depth dimensions of the
# referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
heightDistance = 2.0
widthDistance = 2.0
depthDistance = 0.1

vs.Set3DInfo(h, heightDistance, widthDistance, depthDistance)
```

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
