# TBB_UpdateOldBorders

## Description
Updates Drawing Border - Universal objects to Title Block Border objects.

```pascal
PROCEDURE TBB_UpdateOldBorders(VAR NumUpdated : INTEGER);
```

```python
def vs.TBB_UpdateOldBorders():
    return NumUpdated
```

## Parameters
|Name|Type|Description|
|---|---|---|
|NumUpdated|INTEGER|   |

## Examples
```pascal
{ VAA Title Block }
{ Drawing Border - Universal }
TBB_UpdateOldBorders(gNumBordersUpdated);
```
```python
import vs

# Updates Drawing Border - Universal objects to Title Block Border objects.
result = vs.TBB_UpdateOldBorders()
```

## Version
Availability: from Vectorworks 2018

## Category
* [Utility](../Categories/Utility.md)
