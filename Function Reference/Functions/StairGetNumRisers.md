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

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
