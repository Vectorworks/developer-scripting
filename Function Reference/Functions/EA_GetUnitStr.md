# EA_GetUnitStr

## Description
Returns document unit string.

```pascal
FUNCTION EA_GetUnitStr(unitType : INTEGER): STRING;
```

```python
def vs.EA_GetUnitStr(unitType):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|unitType|INTEGER|   |

## Examples
```pascal
resultStr := EA_GetUnitStr(1);
```
```python
import vs

# Returns document unit string.
unitType = 0

text = vs.EA_GetUnitStr(unitType)
vs.Message('EA_GetUnitStr returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
