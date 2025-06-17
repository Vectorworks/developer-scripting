# GetDropShadowData

```pascal
FUNCTION GetDropShadowData(
				h               : HANDLE;
				VAR nUnits      : INTEGER;
				VAR dOffset     : REAL;
				VAR dBlurRadius : REAL;
				VAR dAngle      : REAL;
				VAR nOpacity    : INTEGER;
				VAR colorRV     : INTEGER;
				VAR colorGV     : INTEGER;
				VAR colorBV     : INTEGER): BOOLEAN;
```

```python
def vs.GetDropShadowData(h):
    return (BOOLEAN, nUnits, dOffset, dBlurRadius, dAngle, nOpacity, colorRV, colorGV, colorBV)
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
|colorRV|INTEGER|   |
|colorGV|INTEGER|   |
|colorBV|INTEGER|   |

## Remarks
[[User:Ptr|Ptr]] [2021.03.02]:
nUnits returns 0 for page units and 1 for world units.

Disregarding the document unit settings, if nUnits = 0, dOffset and dBlurRadius are in inch, if nUnits = 1, dOffset and dBlurRadius are in mm.

[[User:Ptr|Ptr]] [2021.02.22]:
The RGB values out of this call return pretty strange values ranging from -32640 to 32639.
To get them converted to RGB255 values, use:
<code lang="py">
if colorRV > 0:
	colorR = colorRV / 257
else:
	colorR = (colorRV + 65536) / 257
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
