# SetHLLineStyle

## Description
Sets the Line Style of the specified Hidden Line Rendering options handle.

```pascal
PROCEDURE SetHLLineStyle(
				HLOptionsHandle : HANDLE;
				lineStyle       : INTEGER);
```

```python
def vs.SetHLLineStyle(HLOptionsHandle, lineStyle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|HLOptionsHandle|HANDLE|   |
|lineStyle|INTEGER|   |

## Examples
```pascal
SetHLLineStyle(HLOptionsHandle, 1);
```
```python
import vs

# Sets the Line Style of the specified Hidden Line Rendering options handle.
HLOptionsHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
lineStyle = 0

vs.SetHLLineStyle(HLOptionsHandle, lineStyle)
```

## Version
Availability: from Vectorworks 2019

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
