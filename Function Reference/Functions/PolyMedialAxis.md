# PolyMedialAxis

## Description
Creates a group of lines which represent the weighted medial axis of given polygon.

```pascal
FUNCTION PolyMedialAxis(h : HANDLE): HANDLE;
```

```python
def vs.PolyMedialAxis(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
BEGIN
	if polyHandle <> nil then BEGIN
		medAxis := PolyMedialAxis(polyHandle);
		IF medAxis <> NIL THEN MedialAxis := CleanMedialAxis(medAxis, minimumRadius);
	END;
```
```python
import vs

# Creates a group of lines which represent the weighted medial axis of given
# polygon.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.PolyMedialAxis(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
