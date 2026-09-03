# GetWallPreferences

## Description
Gets the Wall Preferences. This can be used with the component calls and the Style selectors.

```pascal
FUNCTION GetWallPreferences : HANDLE;
```

```python
def vs.GetWallPreferences():
    return HANDLE
```

## Examples
```pascal
resultH := GetWallPreferences;
```
```python
import vs

# Gets the Wall Preferences.
objHandle = vs.GetWallPreferences()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
