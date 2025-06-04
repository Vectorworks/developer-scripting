# GetWallCompEndPts

## Description
Gets the end points of a wall component.

```pascal
PROCEDURE GetWallCompEndPts(
				wall            : HANDLE;
				componentIndex  : INTEGER;
				VAR leftPoint   : POINT;
				VAR centerPoint : POINT;
				VAR rightPoint  : POINT);
```

```python
def vs.GetWallCompEndPts(wall, componentIndex):
    return (leftPoint, centerPoint, rightPoint)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The wall or round wall|
|componentIndex|INTEGER|The component index|
|leftPoint|POINT|Returns the left end point of the component|
|centerPoint|POINT|Returns the center end point of the component|
|rightPoint|POINT|Returns the right end point of the component|

## See Also
VS Functions:
[GetWallCompStartPts](GetWallCompStartPts.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
