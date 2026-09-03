# GetSlabPreferences

## Description
Gets the Slab Preferences. This can be used with the component calls and the Style selectors.

```pascal
FUNCTION GetSlabPreferences : HANDLE;
```

```python
def vs.GetSlabPreferences():
    return HANDLE
```

## Examples
```pascal
resultH := GetSlabPreferences;
```
```python
import vs

# Gets the Slab Preferences.
objHandle = vs.GetSlabPreferences()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
