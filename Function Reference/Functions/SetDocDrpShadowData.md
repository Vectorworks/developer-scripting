# SetDocDrpShadowData

```pascal
PROCEDURE SetDocDrpShadowData(
				bUseDropShadow : BOOLEAN;
				nUnits         : INTEGER;
				dOffset        : REAL;
				dBlurRadius    : REAL;
				dAngle         : REAL;
				nOpacity       : INTEGER;
				color          : LONGINT);
```

```python
def vs.SetDocDrpShadowData(bUseDropShadow, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|bUseDropShadow|BOOLEAN|   |
|nUnits|INTEGER|   |
|dOffset|REAL|   |
|dBlurRadius|REAL|   |
|dAngle|REAL|   |
|nOpacity|INTEGER|   |
|color|LONGINT|   |

## Examples
```pascal
SetDocDrpShadowData(TRUE, 1, 1.0, 2.0, 0.5, 2, 3);
```
```python
import vs

bUseDropShadow = True
nUnits = 1
dOffset = 0.0
dBlurRadius = 1.0
dAngle = 45.0
nOpacity = 2
color = 5

vs.SetDocDrpShadowData(bUseDropShadow, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, color)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
