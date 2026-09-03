# EA_ConvX2Doc

## Description
Converts value from X unit to document unit and returns the result as a real number.

```pascal
FUNCTION EA_ConvX2Doc(
				unitType : INTEGER;
				value    : REAL): REAL;
```

```python
def vs.EA_ConvX2Doc(unitType, value):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|unitType|INTEGER|   |
|value|REAL|   |

## Examples
```pascal
resultVal := EA_ConvX2Doc(1, 1.0);
```
```python
import vs

# Converts value from X unit to document unit and returns the result as a
# real number.
unitType = 0
value = 1.0

value = vs.EA_ConvX2Doc(unitType, value)
vs.Message('EA_ConvX2Doc returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
