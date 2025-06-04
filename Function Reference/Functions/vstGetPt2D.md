# vstGetPt2D

## Description
Returns the point clicked by the user. inPtIndex is 0-based. If you pass in an index that is greater than the number of points clicked by the user, result will be false.

```pascal
PROCEDURE vstGetPt2D(
				inPtIndex : LONGINT;
				VAR outX  : REAL;
				VAR outY  : REAL;
				result    : BOOLEAN);
```

```python
def vs.vstGetPt2D(inPtIndex, result):
    return (outX, outY)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPtIndex|LONGINT|   |
|outX|REAL|Output parameter.|
|outY|REAL|Output parameter.|
|result|BOOLEAN|   |

## Remarks
Note that [[VS:vstNumPts]] will return the number of clicked points (a 1-based index). vstGetPt2D is zero-based. So if you're collecting points in the kToolEventPointAdded event you'll likely have to do something like

<code>
 vstNumPoints(pointNum);
 vstGetPt2D(pointNum-1, ...);
</code>

[MaKro 6/2018]: ... with pyhton consider using VS:vstGetCurrPt2D ...

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
