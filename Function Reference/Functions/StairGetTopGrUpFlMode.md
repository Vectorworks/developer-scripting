# StairGetTopGrUpFlMode

## Description
<lineList ident=2>
<line>
Returns top graphic on other floor mode of stair.
</line>

<line>
0: Has no top graphic (proxy object) on upper floor
</line>
<line>
1: Has top graphic (proxy object) on upper floor
</line>
<line>
-1: Error
</line>
</lineList>

```pascal
FUNCTION StairGetTopGrUpFlMode(stair : HANDLE): INTEGER;
```

```python
def vs.StairGetTopGrUpFlMode(stair):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |

## Examples
```pascal
resultN := StairGetTopGrUpFlMode(stair);
```
```python
import vs

# Returns top graphic on other floor mode of stair.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.StairGetTopGrUpFlMode(stair)
vs.Message('StairGetTopGrUpFlMode returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
