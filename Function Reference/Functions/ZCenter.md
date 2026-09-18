# ZCenter

## Description
_[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)_. See [ZCenterN](ZCenterN.md) for a replacement function.

Returns the z-coordinate value of the center of an object matching the search criteria.

```pascal
FUNCTION ZCenter(c : CRITERIA): REAL;
```

```python
def vs.ZCenter(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|   |

## Examples
```pascal
resultVal := ZCenter(c);
```
```python
import vs

# _Vectorworks 2012 Deprecated Functions_.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.ZCenter(c)
vs.Message('ZCenter returned: ' + str(value))
```

## Version
Availability: from Vectorworks14.0
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Criteria](../Categories/Criteria.md)
