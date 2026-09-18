# EA_ConvX2DocStr

## Description
Converts value from X unit to document unit and returns the result as real number.

```pascal
FUNCTION EA_ConvX2DocStr(
				unitType    : INTEGER;
				value       : REAL;
				incUnitMark : BOOLEAN): STRING;
```

```python
def vs.EA_ConvX2DocStr(unitType, value, incUnitMark):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|unitType|INTEGER|   |
|value|REAL|   |
|incUnitMark|BOOLEAN|   |

## Examples
```pascal
resultStr := EA_ConvX2DocStr(1, 1.0, TRUE);
```
```python
import vs

# Converts value from X unit to document unit and returns the result as real
# number.
unitType = 0
value = 1.0
incUnitMark = True

text = vs.EA_ConvX2DocStr(unitType, value, incUnitMark)
vs.Message('EA_ConvX2DocStr returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
