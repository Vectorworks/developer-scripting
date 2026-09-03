# StairGetNumRisers

## Description
Returns numbers of risers of stair flights 1-4. Returns -1 in case of error and for flights that don't exist.

```pascal
FUNCTION StairGetNumRisers(
				stair          : HANDLE;
				VAR NumRisers1 : INTEGER;
				VAR NumRisers2 : INTEGER;
				VAR NumRisers3 : INTEGER;
				VAR NumRisers4 : INTEGER): BOOLEAN;
```

```python
def vs.StairGetNumRisers(stair):
    return (BOOLEAN, NumRisers1, NumRisers2, NumRisers3, NumRisers4)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |
|NumRisers1|INTEGER|   |
|NumRisers2|INTEGER|   |
|NumRisers3|INTEGER|   |
|NumRisers4|INTEGER|   |

## Examples
```pascal
resultOK := StairGetNumRisers(stair, 1, 2, 3, 10);
```
```python
import vs

# Returns numbers of risers of stair flights 1-4.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, NumRisers1, NumRisers2, NumRisers3, NumRisers4 = vs.StairGetNumRisers(stair)
vs.Message('StairGetNumRisers returned: ' + str((ok, NumRisers1, NumRisers2, NumRisers3, NumRisers4)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
