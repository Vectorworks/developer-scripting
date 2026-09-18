# SetDropShadowData

```pascal
PROCEDURE SetDropShadowData(
				h           : HANDLE;
				nUnits      : INTEGER;
				dOffset     : REAL;
				dBlurRadius : REAL;
				dAngle      : REAL;
				nOpacity    : INTEGER;
				color       : LONGINT);
```

```python
def vs.SetDropShadowData(h, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|nUnits|INTEGER|   |
|dOffset|REAL|   |
|dBlurRadius|REAL|   |
|dAngle|REAL|   |
|nOpacity|INTEGER|   |
|color|LONGINT|   |

## Examples
```pascal
SetDropShadowData(h, 1, 1.0, 2.0, 0.5, 2, 3);
```
```python
import vs

h = vs.FSActLayer()  # handle to the first selected object on the active layer
nUnits = 1
dOffset = 0.0
dBlurRadius = 1.0
dAngle = 45.0
nOpacity = 2
color = 5

vs.SetDropShadowData(h, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, color)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
