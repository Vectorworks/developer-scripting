# GetRRDiam

## Description
Procedure GetRRDiam returns the horizontal and vertical diameters of the rounded corners of a rounded rectangle object.

```pascal
PROCEDURE GetRRDiam(
				h         : HANDLE;
				VAR xDiam : REAL;
				VAR yDiam : REAL);
```

```python
def vs.GetRRDiam(h):
    return (xDiam, yDiam)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|xDiam|REAL|X diameter of rounded corner.|
|yDiam|REAL|Y diameter of rounded corner.|

## Examples
```pascal
GetRRDiam(h, 1.0, 2.0);
```
```python
import vs

# Procedure GetRRDiam returns the horizontal and vertical diameters of the
# rounded corners of a rounded rectangle object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

xDiam, yDiam = vs.GetRRDiam(h)
vs.Message('GetRRDiam returned: ' + str((xDiam, yDiam)))
```

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
