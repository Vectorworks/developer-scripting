# GetOriginInDocUnits

## Description
Procedure GetOriginInDocUnits returns the current origin location relative to the center of the page in current units. It fixes the problem existing for GetOrigin (see remarks). The behavior is the same while used during objects reset and in commands.

```pascal
PROCEDURE GetOriginInDocUnits(
				VAR x : REAL;
				VAR y : REAL);
```

```python
def vs.GetOriginInDocUnits():
    return (x, y)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x|REAL|Returns X coordinate of origin.|
|y|REAL|Returns Y coordinate of origin.|

## Examples
```pascal
PROCEDURE Example;
VAR
originPt : VECTOR;
BEGIN
GetOriginInDocUnits(originPt.x, originPt.y);
Message(originPt);
END;
RUN(Example);
```

```pascal
GetOriginInDocUnits(1.0, 2.0);
```
```python
import vs

# Procedure GetOriginInDocUnits returns the current origin location relative
# to the center of the page in current units.
x, y = vs.GetOriginInDocUnits()
vs.Message('GetOriginInDocUnits returned: ' + str((x, y)))
```

## See Also
VS Functions:
[GetOrigin](GetOrigin.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Document Settings](../Categories/Document%20Settings.md)
