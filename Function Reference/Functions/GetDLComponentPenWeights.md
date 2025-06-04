# GetDLComponentPenWeights

## Description
Gets the pen weights of the left and right sides of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLComponentPenWeights(
				index              : INTEGER;
				VAR penWeightLeft  : INTEGER;
				VAR penWeightRight : INTEGER): BOOLEAN;
```

```python
def vs.GetDLComponentPenWeights(index):
    return (BOOLEAN, penWeightLeft, penWeightRight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|penWeightLeft|INTEGER|Returns the pen weight of the component's left line.|
|penWeightRight|INTEGER|Returns the pen weight of the component's right line.|

## Remarks
CJG 6-27-06

## See Also
VS Functions:
[SetDLComponentPenWeights](SetDLComponentPenWeights.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
