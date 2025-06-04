# GetNumOfWallBreaks

## Description
Gets the number of breaks in a wall.

```pascal
FUNCTION GetNumOfWallBreaks(
				wallH             : HANDLE;
				VAR numWallBreaks : INTEGER): BOOLEAN;
```

```python
def vs.GetNumOfWallBreaks(wallH):
    return (BOOLEAN, numWallBreaks)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallH|HANDLE|   |
|numWallBreaks|INTEGER|   |

## Remarks
This currently fails on Round Walls. (VW 13.01+).

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
