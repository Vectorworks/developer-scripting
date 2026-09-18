# SetCLDrpShadowData

```pascal
PROCEDURE SetCLDrpShadowData(
				className   : STRING;
				nUnits      : INTEGER;
				dOffset     : REAL;
				dBlurRadius : REAL;
				dAngle      : REAL;
				nOpacity    : INTEGER;
				color       : LONGINT);
```

```python
def vs.SetCLDrpShadowData(className, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|   |
|nUnits|INTEGER|   |
|dOffset|REAL|   |
|dBlurRadius|REAL|   |
|dAngle|REAL|   |
|nOpacity|INTEGER|   |
|color|LONGINT|   |

## Remarks
[[User:Ptr|Ptr]] [2021.03.02]:
nUnits returns 0 for page units and 1 for world units.

If nUnits = 0, dOffset and dBlurRadius are in inch, if nUnits = 1, dOffset and dBlurRadius are in document units.

## Examples
```pascal
SetCLDrpShadowData('Wall', 1, 1.0, 2.0, 0.5, 2, 3);
```
```python
import vs

className = 'None'
nUnits = 1
dOffset = 0.0
dBlurRadius = 1.0
dAngle = 45.0
nOpacity = 2
color = 5

vs.SetCLDrpShadowData(className, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, color)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Classes](../Categories/Classes.md)
