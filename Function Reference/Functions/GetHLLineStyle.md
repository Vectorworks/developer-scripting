# GetHLLineStyle

## Description
Gets the Line Style of the specified Hidden Line Rendering options handle.

```pascal
PROCEDURE GetHLLineStyle(
				HLOptionsHandle : HANDLE;
				VAR lineStyle   : INTEGER);
```

```python
def vs.GetHLLineStyle(HLOptionsHandle):
    return lineStyle
```

## Parameters
|Name|Type|Description|
|---|---|---|
|HLOptionsHandle|HANDLE|   |
|lineStyle|INTEGER|   |

## Examples
```pascal
GetHLLineStyle(HLOptionsHandle, 1);
```
```python
import vs

# Gets the Line Style of the specified Hidden Line Rendering options handle.
HLOptionsHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.GetHLLineStyle(HLOptionsHandle)
```

## Version
Availability: from Vectorworks 2019

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
