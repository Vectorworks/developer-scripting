# SetComponentPenWeights

## Description
Sets the left and right pen weights for a component in an object.

```pascal
FUNCTION SetComponentPenWeights(
				obj            : HANDLE;
				componentIndex : INTEGER;
				leftPenWeight  : INTEGER;
				rightPenWeight : INTEGER): BOOLEAN;
```

```python
def vs.SetComponentPenWeights(obj, componentIndex, leftPenWeight, rightPenWeight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|leftPenWeight|INTEGER|The pen weight of the component's left line.|
|rightPenWeight|INTEGER|The pen weight of the component's right line.|

## Remarks
VW2011: It seems that the right line doesn't get adjusted...

## Examples
```pascal
resultOK := SetComponentPenWeights(obj, 1, 2, 3);
```
```python
import vs

# Sets the left and right pen weights for a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
leftPenWeight = 1
rightPenWeight = 2

ok = vs.SetComponentPenWeights(obj, componentIndex, leftPenWeight, rightPenWeight)
if ok:
    vs.Message('SetComponentPenWeights succeeded')
else:
    vs.Message('SetComponentPenWeights failed')
```

## See Also
VS Functions:
[GetComponentPenWeights](GetComponentPenWeights.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
