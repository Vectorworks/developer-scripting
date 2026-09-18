# EA_ConvStr2X

## Description
Converts string to X unit and returns the result as real number.

```pascal
FUNCTION EA_ConvStr2X(
				unitType : INTEGER;
				value    : STRING): REAL;
```

```python
def vs.EA_ConvStr2X(unitType, value):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|unitType|INTEGER|   |
|value|STRING|   |

## Examples
```pascal
resultVal := EA_ConvStr2X(1, 'Example');
```
```python
import vs

# Converts string to X unit and returns the result as real number.
unitType = 0
value = 'Example'

value = vs.EA_ConvStr2X(unitType, value)
vs.Message('EA_ConvStr2X returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
