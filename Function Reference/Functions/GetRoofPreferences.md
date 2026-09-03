# GetRoofPreferences

## Description
Gets the Roof Preferences. This can be used with the component calls and the Style selectors.

```pascal
FUNCTION GetRoofPreferences : HANDLE;
```

```python
def vs.GetRoofPreferences():
    return HANDLE
```

## Examples
```pascal
resultH := GetRoofPreferences;
```
```python
import vs

# Gets the Roof Preferences.
objHandle = vs.GetRoofPreferences()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
