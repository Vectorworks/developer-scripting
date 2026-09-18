# EA_DataAccGetInt

## Description
Returns integer value from the object, associated to the accessory index.

```pascal
FUNCTION EA_DataAccGetInt(
				acc        : INTEGER;
				valueIndex : INTEGER): INTEGER;
```

```python
def vs.EA_DataAccGetInt(acc, valueIndex):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|valueIndex|INTEGER|   |

## Examples
```pascal
resultN := EA_DataAccGetInt(1, 2);
```
```python
import vs

# Returns integer value from the object, associated to the accessory index.
acc = 1
valueIndex = 1

resultN = vs.EA_DataAccGetInt(acc, valueIndex)
vs.Message('EA_DataAccGetInt returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
