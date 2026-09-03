# SetDLComponentPenWeights

## Description
Sets the left and right pen weights for the component at index in the Double Line Preferences.

```pascal
FUNCTION SetDLComponentPenWeights(
				index          : INTEGER;
				penWeightLeft  : INTEGER;
				penWeightRight : INTEGER): BOOLEAN;
```

```python
def vs.SetDLComponentPenWeights(index, penWeightLeft, penWeightRight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|penWeightLeft|INTEGER|The pen weight of the component's left line.|
|penWeightRight|INTEGER|The pen weight of the component's right line.|

## Remarks
CJG 6-27-06

## Examples
```pascal
resultOK := SetDLComponentPenWeights(1, 2, 3);
```
```python
import vs

# Sets the left and right pen weights for the component at index in the
# Double Line Preferences.
index = 1
penWeightLeft = 1
penWeightRight = 2

ok = vs.SetDLComponentPenWeights(index, penWeightLeft, penWeightRight)
if ok:
    vs.Message('SetDLComponentPenWeights succeeded')
else:
    vs.Message('SetDLComponentPenWeights failed')
```

## See Also
VS Functions:
[GetDLComponentPenWeights](GetDLComponentPenWeights.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
