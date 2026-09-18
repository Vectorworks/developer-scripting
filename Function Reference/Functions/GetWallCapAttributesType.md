# GetWallCapAttributesType

## Description
Gets the wall cap attributes type of a wall or round wall.  The wall cap attributes type determines whether the wall caps have the wall line attributes or the component lines attributes.  If they have the component lines attributes, each wall component is capped with its own left line attributes.

```pascal
FUNCTION GetWallCapAttributesType(wall : HANDLE): INTEGER;
```

```python
def vs.GetWallCapAttributesType(wall):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The handle to the wall or round wall.|

## Examples
```pascal
resultN := GetWallCapAttributesType(wall);
```
```python
import vs

# Gets the wall cap attributes type of a wall or round wall.
wall = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetWallCapAttributesType(wall)
vs.Message('GetWallCapAttributesType returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetWallCapAttributesType](SetWallCapAttributesType.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
