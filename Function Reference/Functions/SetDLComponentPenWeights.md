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

## See Also
VS Functions:
[GetDLComponentPenWeights](GetDLComponentPenWeights.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
