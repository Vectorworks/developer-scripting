# HO_GetNumHoistOrigin

## Description
Get the number of all Hoist Origin objects in the current document

```pascal
FUNCTION HO_GetNumHoistOrigin : LONGINT;
```

```python
def vs.HO_GetNumHoistOrigin():
    return LONGINT
```

## Examples
```pascal
resultN := HO_GetNumHoistOrigin;
```
```python
import vs

# Get the number of all Hoist Origin objects in the current document.
count = vs.HO_GetNumHoistOrigin()
vs.Message('HO_GetNumHoistOrigin returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Spotlight](../Categories/Spotlight.md)
