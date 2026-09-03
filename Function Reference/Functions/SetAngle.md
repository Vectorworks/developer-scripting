# SetAngle

## Description
Set angle of the passed object.

```pascal
PROCEDURE SetAngle(
				h     : HANDLE;
				value : REAL);
```

```python
def vs.SetAngle(h, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|value|REAL|The new rotation angle of the object. Angle in degrees (-180;180] measured from (1,0) vector.|

## Examples
```pascal
SetAngle(h, 1.0);
```
```python
import vs

# Set angle of the passed object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
value = 1.0

vs.SetAngle(h, value)
```

## Version
Availability: from Vectorworks14.0

## Category
* [Object Info](../Categories/Object%20Info.md)
