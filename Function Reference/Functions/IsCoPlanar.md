# IsCoPlanar

## Description
Returns true if two planes are coplanar.

```pascal
FUNCTION IsCoPlanar(
				refID1 : LONGINT;
				refID2 : LONGINT): BOOLEAN;
```

```python
def vs.IsCoPlanar(refID1, refID2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|refID1|LONGINT|Reference ID of the first plane.|
|refID2|LONGINT|Reference ID of the second plane.|

## Examples
```pascal
resultOK := IsCoPlanar(1, 2);
```
```python
import vs

# Returns true if two planes are coplanar.
refID1 = 1
refID2 = 2

ok = vs.IsCoPlanar(refID1, refID2)
if ok:
    vs.Message('IsCoPlanar succeeded')
else:
    vs.Message('IsCoPlanar failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
