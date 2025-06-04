# GetNumDashDataPairsN

## Description
Function GetNumDashDataPairsN returns the number of dash/gap value pairs defined for the specified dash style. The &quot;scale with thickness&quot; setting is also returned. Dash styles support up to 5 dash/gap value pairs.

```pascal
FUNCTION GetNumDashDataPairsN(
				dashIndex : LONGINT;
				VAR swt   : BOOLEAN): INTEGER;
```

```python
def vs.GetNumDashDataPairsN(dashIndex):
    return (INTEGER, swt)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dashIndex|LONGINT|The negative value of the dash pattern's internal index.|
|swt|BOOLEAN|The &quot;scale with thickness&quot; setting.|

## Examples
```python
PROCEDURE Example;
VAR
n, numPairs : INTEGER;
dashIndex : LONGINT;
scaleWThick  :BOOLEAN;
arrayDashDat : ARRAY[1..5] OF POINT;
x,y : REAL;

BEGIN

dashIndex := GetDashStyleIndexN(TRUE, 2, 0.12, 0.18, 0.03, 0.07);

numPairs := GetNumDashDataPairsN(dashIndex,scaleWThick);

FOR n := 1 TO numPairs DO BEGIN
 IF (GetDashDataValPrAtN(dashIndex, n , x, y)) THEN BEGIN
   arrayDashDat[n].x := x ;
   arrayDashDat[n].y := y ;
 END; 
END;

END;
RUN(Example);
```

## See Also
VS Functions:
[GetDashDataValPrAtN](GetDashDataValPrAtN.md) 
| [GetDashStyleIndexN](GetDashStyleIndexN.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
