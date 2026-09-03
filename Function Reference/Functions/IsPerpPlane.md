# IsPerpPlane

## Description
Returns true if two planes are perpendicular.

```pascal
FUNCTION IsPerpPlane(
				refID1 : LONGINT;
				refID2 : LONGINT): BOOLEAN;
```

```python
def vs.IsPerpPlane(refID1, refID2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|refID1|LONGINT|Reference ID of the first plane.|
|refID2|LONGINT|Reference ID of the second plane.|

## Examples
```pascal
resultOK := IsPerpPlane(1, 2);
```
```python
import vs

# Returns true if two planes are perpendicular.
refID1 = 1
refID2 = 2

ok = vs.IsPerpPlane(refID1, refID2)
if ok:
    vs.Message('IsPerpPlane succeeded')
else:
    vs.Message('IsPerpPlane failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
