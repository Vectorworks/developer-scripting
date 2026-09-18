# StairSetNumRisers

## Description
Sets numbers of risers of stair flights 1-4 - not recommended for use as stair might end up with inconsistent and contradictory parameters.

```pascal
FUNCTION StairSetNumRisers(
				stair      : HANDLE;
				NumRisers1 : INTEGER;
				NumRisers2 : INTEGER;
				NumRisers3 : INTEGER;
				NumRisers4 : INTEGER): BOOLEAN;
```

```python
def vs.StairSetNumRisers(stair, NumRisers1, NumRisers2, NumRisers3, NumRisers4):
    return BOOLEAN
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
resultOK := StairSetNumRisers(stair, 1, 2, 3, 10);
```
```python
import vs

# Sets numbers of risers of stair flights 1-4 - not recommended for use as
# stair might end up with inconsistent and contradictory parameters.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer
NumRisers1 = 5
NumRisers2 = 5
NumRisers3 = 5
NumRisers4 = 5

ok = vs.StairSetNumRisers(stair, NumRisers1, NumRisers2, NumRisers3, NumRisers4)
if ok:
    vs.Message('StairSetNumRisers succeeded')
else:
    vs.Message('StairSetNumRisers failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
