# SetSlabPreferencesStyle

## Description
Sets the Slab Style of the Slab Preferences.

```pascal
PROCEDURE SetSlabPreferencesStyle(slabStyle : LONGINT);
```

```python
def vs.SetSlabPreferencesStyle(slabStyle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|slabStyle|LONGINT|The ref number of the Slab Style to apply to the Slab Preferences. 0 for unstyled.|

## Examples
```pascal
SetSlabPreferencesStyle(1);
```
```python
import vs

# Sets the Slab Style of the Slab Preferences.
slabStyle = 0

vs.SetSlabPreferencesStyle(slabStyle)
```

## See Also
VS Functions:
[GetSlabPreferencesStyle](GetSlabPreferencesStyle.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
