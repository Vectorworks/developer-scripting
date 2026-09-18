# EA_DataAccSetBool

## Description
Set boolean value to the object, associated to the accessory index.

```pascal
PROCEDURE EA_DataAccSetBool(
				acc        : INTEGER;
				valueIndex : INTEGER;
				value      : BOOLEAN);
```

```python
def vs.EA_DataAccSetBool(acc, valueIndex, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|valueIndex|INTEGER|   |
|value|BOOLEAN|   |

## Examples
```pascal
EA_DataAccSetBool(1, 2, TRUE);
```
```python
import vs

# Set boolean value to the object, associated to the accessory index.
acc = 1
valueIndex = 1
value = True

vs.EA_DataAccSetBool(acc, valueIndex, value)
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
