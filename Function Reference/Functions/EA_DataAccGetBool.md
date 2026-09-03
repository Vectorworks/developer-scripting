# EA_DataAccGetBool

## Description
Returns boolean value from the object, associated to the accessory index.

```pascal
FUNCTION EA_DataAccGetBool(
				acc        : INTEGER;
				valueIndex : INTEGER): BOOLEAN;
```

```python
def vs.EA_DataAccGetBool(acc, valueIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|valueIndex|INTEGER|   |

## Examples
```pascal
resultOK := EA_DataAccGetBool(1, 2);
```
```python
import vs

# Returns boolean value from the object, associated to the accessory index.
acc = 1
valueIndex = 1

ok = vs.EA_DataAccGetBool(acc, valueIndex)
if ok:
    vs.Message('EA_DataAccGetBool succeeded')
else:
    vs.Message('EA_DataAccGetBool failed')
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
