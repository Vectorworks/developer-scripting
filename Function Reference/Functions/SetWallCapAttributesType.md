# SetWallCapAttributesType

## Description
Sets the wall cap attributes type of a wall or round wall.  The wall cap attributes type determines whether the wall caps have the wall line attributes or the component lines attributes.  If they have the component lines attributes, each wall component is capped with its own left line attributes.

```pascal
PROCEDURE SetWallCapAttributesType(
				wall                  : HANDLE;
				wallCapAttributesType : INTEGER);
```

```python
def vs.SetWallCapAttributesType(wall, wallCapAttributesType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The handle to the wall or round wall.|
|wallCapAttributesType|INTEGER|The wall cap attributes type.||0 - The wall cap attributes are the wall line attributes|1 - The wall cap attributes are the wall component lines attributes|

## Examples
```pascal
SetWallCapAttributesType(wall, 1);
```
```python
import vs

# Sets the wall cap attributes type of a wall or round wall.
wall = vs.FSActLayer()  # handle to the first selected object on the active layer
wallCapAttributesType = 0

vs.SetWallCapAttributesType(wall, wallCapAttributesType)
```

## See Also
VS Functions:
[GetWallCapAttributesType](GetWallCapAttributesType.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
