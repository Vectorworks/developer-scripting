# GetComponentManualEdgeOffset

## Description
Gets the manual edge offset of a component in an object.

```pascal
FUNCTION GetComponentManualEdgeOffset(
				obj                  : HANDLE;
				componentIndex       : INTEGER;
				VAR manualEdgeOffset : REAL): BOOLEAN;
```

```python
def vs.GetComponentManualEdgeOffset(obj, componentIndex):
    return (BOOLEAN, manualEdgeOffset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a  slab, Slab Style, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|manualEdgeOffset|REAL|Returns the manual edge offset.|

## See Also
VS Functions:
[SetComponentManualEdgeOffset](SetComponentManualEdgeOffset.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
