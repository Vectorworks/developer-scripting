# OffsetPolyClosed

## Description
Offsets a polyline or polygon, then uses the original geometry to construct a closed profile.

```pascal
FUNCTION OffsetPolyClosed(
				obj           : HANDLE;
				offset        : REAL;
				smoothCorners : BOOLEAN): HANDLE;
```

```python
def vs.OffsetPolyClosed(obj, offset, smoothCorners):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|offset|REAL|   |
|smoothCorners|BOOLEAN|   |

## Remarks
'''Notes:''' (ptr - 2020 apr 10)
The offset is always in mm. So please convert your document units to mm:
```python
result = vs.OffsetPolyClosed(obj, offset /vs.GetPrefReal(152)*25.4, smoothCorners)
```

## Examples
```pascal
IF(clipFill)
THEN BEGIN
	hOriginalPoly 	:= LnewObj;
	hOffsetPoly 	:= OffsetPolyClosed(LnewObj, -1, False);
```
```python
import vs

# Offsets a polyline or polygon, then uses the original geometry to construct
# a closed profile.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
offset = 0.0
smoothCorners = True

objHandle = vs.OffsetPolyClosed(obj, offset, smoothCorners)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
