# GetWallCompStartPts

## Description
Gets the start points of a wall component.

```pascal
PROCEDURE GetWallCompStartPts(
				wall            : HANDLE;
				componentIndex  : INTEGER;
				VAR leftPoint   : POINT;
				VAR centerPoint : POINT;
				VAR rightPoint  : POINT);
```

```python
def vs.GetWallCompStartPts(wall, componentIndex):
    return (leftPoint, centerPoint, rightPoint)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The wall or round wall|
|componentIndex|INTEGER|The component index|
|leftPoint|POINT|Returns the left start point of the component|
|centerPoint|POINT|Returns the center start point of the component|
|rightPoint|POINT|Returns the right start point of the component|

## See Also
VS Functions:
[GetWallCompEndPts](GetWallCompEndPts.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
