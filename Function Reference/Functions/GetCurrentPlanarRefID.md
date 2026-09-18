# GetCurrentPlanarRefID

## Description
Return the current plane ref ID. This could be any plane: a working plane, screen plane (0), ground plane of a container, or any arbitrary plane.

```pascal
FUNCTION GetCurrentPlanarRefID : LONGINT;
```

```python
def vs.GetCurrentPlanarRefID():
    return LONGINT
```

## Examples
```pascal
resultN := GetCurrentPlanarRefID;
```
```python
import vs

# Return the current plane ref ID.
resultN = vs.GetCurrentPlanarRefID()
vs.Message('GetCurrentPlanarRefID returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Document Settings](../Categories/Document%20Settings.md)
