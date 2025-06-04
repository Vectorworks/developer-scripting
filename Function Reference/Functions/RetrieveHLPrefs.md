# RetrieveHLPrefs

## Description
Retrieves the current Hidden Line rendering preferences from data stored in the current drawing.

```pascal
PROCEDURE RetrieveHLPrefs(
				VAR smoothingAngle   : REAL;
				VAR lineStyle        : INTEGER;
				VAR shadeFactorIndex : INTEGER;
				VAR doIntersections  : BOOLEAN);
```

```python
def vs.RetrieveHLPrefs():
    return (smoothingAngle, lineStyle, shadeFactorIndex, doIntersections)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|smoothingAngle|REAL|   |
|lineStyle|INTEGER|   |
|shadeFactorIndex|INTEGER|   |
|doIntersections|BOOLEAN|   |

## Version
Availability: from Vectorworks 2014

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
