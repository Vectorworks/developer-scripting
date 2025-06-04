# GetWallPeak

## Description
Returns the coordinates of a wall peak in the referenced wall.

```pascal
PROCEDURE GetWallPeak(
				h         : HANDLE;
				index     : INTEGER;
				VAR xPeak : REAL;
				VAR yPeak : REAL;
				VAR zPeak : REAL);
```

```python
def vs.GetWallPeak(h, index):
    return (xPeak, yPeak, zPeak)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to wall.|
|index|INTEGER|Index of wall peak.|
|xPeak|REAL|X-coordinate of wall peak.|
|yPeak|REAL|Y-coordinate of wall peak.|
|zPeak|REAL|Z-coordinate of wall peak.|

## Remarks
Get xyz values of peak in wall


From Lamberto Previati: GetWallPeak doesn't work if there is a symbol at the same point in the wall as the peak. [This has not been verified.]

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
