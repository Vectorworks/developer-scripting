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

## Examples
```pascal
RetrieveHLPrefs(1.0, 1, 2, TRUE);
```
```python
import vs

# Retrieves the current Hidden Line rendering preferences from data stored in
# the current drawing.
smoothingAngle, lineStyle, shadeFactorIndex, doIntersections = vs.RetrieveHLPrefs()
vs.Message('RetrieveHLPrefs returned: ' + str((smoothingAngle, lineStyle, shadeFactorIndex, doIntersections)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
