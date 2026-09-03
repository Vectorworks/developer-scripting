# SetRoofPrefStyle

## Description
Sets the Roof Style of the Roof Preferences.

```pascal
PROCEDURE SetRoofPrefStyle(roofStyle : LONGINT);
```

```python
def vs.SetRoofPrefStyle(roofStyle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofStyle|LONGINT|The ref number of the Roof Style to apply to the Roof Preferences. 0 for unstyled.|

## Examples
```pascal
SetRoofPrefStyle(1);
```
```python
import vs

# Sets the Roof Style of the Roof Preferences.
roofStyle = 0

vs.SetRoofPrefStyle(roofStyle)
```

## See Also
VS Functions:
[GetRoofPrefStyle](GetRoofPrefStyle.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
