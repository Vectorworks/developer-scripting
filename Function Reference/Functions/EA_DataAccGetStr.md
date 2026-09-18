# EA_DataAccGetStr

## Description
Returns string value from the object, associated to the accessory index.

```pascal
FUNCTION EA_DataAccGetStr(
				acc        : INTEGER;
				valueIndex : INTEGER): STRING;
```

```python
def vs.EA_DataAccGetStr(acc, valueIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|valueIndex|INTEGER|   |

## Examples
```pascal
resultStr := EA_DataAccGetStr(1, 2);
```
```python
import vs

# Returns string value from the object, associated to the accessory index.
acc = 1
valueIndex = 1

text = vs.EA_DataAccGetStr(acc, valueIndex)
vs.Message('EA_DataAccGetStr returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
