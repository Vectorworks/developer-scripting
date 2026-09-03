# GetCLDrpShadowData

```pascal
PROCEDURE GetCLDrpShadowData(
				className       : STRING;
				VAR nUnits      : INTEGER;
				VAR dOffset     : REAL;
				VAR dBlurRadius : REAL;
				VAR dAngle      : REAL;
				VAR nOpacity    : INTEGER;
				VAR colorRV     : INTEGER;
				VAR colorGV     : INTEGER;
				VAR colorBV     : INTEGER);
```

```python
def vs.GetCLDrpShadowData(className):
    return (nUnits, dOffset, dBlurRadius, dAngle, nOpacity, colorRV, colorGV, colorBV)
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
|colorRV|INTEGER|   |
|colorGV|INTEGER|   |
|colorBV|INTEGER|   |

## Examples
```pascal
GetCLDrpShadowData('Wall', 1, 1.0, 2.0, 0.5, 2, 3, 10, 5);
```
```python
import vs

className = 'None'

nUnits, dOffset, dBlurRadius, dAngle, nOpacity, colorRV, colorGV, colorBV = vs.GetCLDrpShadowData(className)
vs.Message('GetCLDrpShadowData returned: ' + str((nUnits, dOffset, dBlurRadius, dAngle, nOpacity, colorRV, colorGV, colorBV)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Classes](../Categories/Classes.md)
