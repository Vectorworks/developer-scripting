# Get3DInfo

## Description
Procedure Get3DInfo returns the height, width and depth values of the referenced 3D object.

```pascal
PROCEDURE Get3DInfo(
				h          : HANDLE;
				VAR height : REAL;
				VAR width  : REAL;
				VAR depth  : REAL);
```

```python
def vs.Get3DInfo(h):
    return (height, width, depth)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to 3D object.|
|height|REAL|Height of object.|
|width|REAL|Width of object.|
|depth|REAL|Depth of object.|

## Remarks
The "height, width, depth" order of the parameters in this call is misleading. The call returns delta-Y, delta-X and delta-Z IN THAT ORDER. Screwy, I know. The example is not a good one because it makes no use of the X and Y data.

## Examples
nipulate3DObjects}}

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
