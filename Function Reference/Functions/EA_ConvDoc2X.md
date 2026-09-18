# EA_ConvDoc2X

## Description
Converts value from document unit to X unit and returns the result as real number.

```pascal
FUNCTION EA_ConvDoc2X(
				unitType : INTEGER;
				value    : REAL): REAL;
```

```python
def vs.EA_ConvDoc2X(unitType, value):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|unitType|INTEGER|   |
|value|REAL|   |

## Examples
```pascal
resultVal := EA_ConvDoc2X(1, 1.0);
```
```python
import vs

# Converts value from document unit to X unit and returns the result as real
# number.
unitType = 0
value = 1.0

value = vs.EA_ConvDoc2X(unitType, value)
vs.Message('EA_ConvDoc2X returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
