# GetDocDrpShadowData

```pascal
PROCEDURE GetDocDrpShadowData(
				VAR bUseDropShadow : BOOLEAN;
				VAR nUnits         : INTEGER;
				VAR dOffset        : REAL;
				VAR dBlurRadius    : REAL;
				VAR dAngle         : REAL;
				VAR nOpacity       : INTEGER;
				VAR colorRV        : INTEGER;
				VAR colorGV        : INTEGER;
				VAR colorBV        : INTEGER);
```

```python
def vs.GetDocDrpShadowData():
    return (bUseDropShadow, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, colorRV, colorGV, colorBV)
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
|colorRV|INTEGER|   |
|colorGV|INTEGER|   |
|colorBV|INTEGER|   |

## Examples
```pascal
GetDocDrpShadowData(TRUE, 1, 1.0, 2.0, 0.5, 2, 3, 10, 5);
```
```python
import vs

bUseDropShadow, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, colorRV, colorGV, colorBV = vs.GetDocDrpShadowData()
vs.Message('GetDocDrpShadowData returned: ' + str((bUseDropShadow, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, colorRV, colorGV, colorBV)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
