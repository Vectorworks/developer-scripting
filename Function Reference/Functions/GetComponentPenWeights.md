# GetComponentPenWeights

## Description
Gets the pen weights of the left and right sides of a component in an object.

```pascal
FUNCTION GetComponentPenWeights(
				obj                : HANDLE;
				componentIndex     : INTEGER;
				VAR leftPenWeight  : INTEGER;
				VAR rightPenWeight : INTEGER): BOOLEAN;
```

```python
def vs.GetComponentPenWeights(obj, componentIndex):
    return (BOOLEAN, leftPenWeight, rightPenWeight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|leftPenWeight|INTEGER|Returns the pen weight of the component's left line.|
|rightPenWeight|INTEGER|Returns the pen weight of the component's right line.|

## See Also
VS Functions:
[SetComponentPenWeights](SetComponentPenWeights.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
