# GetNumDashDataPairs

## Description
Function GetNumDashDataPairs returns the number of dash/gap value pairs defined for the specified dash style. The &quot;scale with thickness&quot; setting is also returned. Dash styles support up to 5 dash/gap value pairs.

```pascal
FUNCTION GetNumDashDataPairs(
				dashIndex : INTEGER;
				VAR swt   : BOOLEAN): INTEGER;
```

```python
def vs.GetNumDashDataPairs(dashIndex):
    return (INTEGER, swt)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dashIndex|INTEGER|The dash style index.|
|swt|BOOLEAN|The &quot;scale with thickness&quot; setting.|

## Examples
```python
PROCEDURE Example;
VAR
n, numPairs, dashIndex : INTEGER;
scaleWThick  :BOOLEAN;
arrayDashDat : ARRAY[1..5] OF POINT;
x,y : REAL;

BEGIN

dashIndex := GetDashStyleIndex(TRUE, 2, 0.12, 0.18, 0.03, 0.07);

numPairs := GetNumDashDataPairs(dashIndex,scaleWThick);

FOR n := 1 TO numPairs DO BEGIN
 IF (GetDashDataValPairAt(dashIndex, n , x, y)) THEN BEGIN
   arrayDashDat[n].x := x ;
   arrayDashDat[n].y := y ;
 END; 
END;

END;
RUN(Example);
```

## See Also
VS Functions:
[GetDashDataValPairAt](GetDashDataValPairAt.md) 
| [GetDashStyleIndex](GetDashStyleIndex.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
