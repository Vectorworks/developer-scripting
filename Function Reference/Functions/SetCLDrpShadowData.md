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

## Version
Availability: from Vectorworks 2017

## Category
* [Classes](../Categories/Classes.md)
