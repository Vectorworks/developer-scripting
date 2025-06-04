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
```python
PROCEDURE Example;
VAR
originPt : VECTOR;
BEGIN
GetOriginInDocUnits(originPt.x, originPt.y);
Message(originPt);
END;
RUN(Example);
```

## See Also
VS Functions:
[GetOrigin](GetOrigin.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Document Settings](../Categories/Document%20Settings.md)
