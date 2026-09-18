# EA_DataAccGetReal

## Description
Returns real value from the object, associated to the accessory index.

```pascal
FUNCTION EA_DataAccGetReal(
				acc        : INTEGER;
				valueIndex : INTEGER): REAL;
```

```python
def vs.EA_DataAccGetReal(acc, valueIndex):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|valueIndex|INTEGER|   |

## Examples
```pascal
resultVal := EA_DataAccGetReal(1, 2);
```
```python
import vs

# Returns real value from the object, associated to the accessory index.
acc = 1
valueIndex = 1

value = vs.EA_DataAccGetReal(acc, valueIndex)
vs.Message('EA_DataAccGetReal returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
