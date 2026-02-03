# GetDashDataValPrAtN

## Description
Function GetDashDataValPrAtN gets the dash data for the specified dash style. The dash data is a dash/gap value pair. GetDashDataValPrAtN returns false if the dash style or dash data doesn't exist. Dash styles support up to 5 dash/gap value pairs.

```pascal
FUNCTION GetDashDataValPrAtN(
				dashStyleIndex : LONGINT;
				dataIndex      : INTEGER;
				VAR dash       : REAL;
				VAR gap        : REAL): BOOLEAN;
```

```python
def vs.GetDashDataValPrAtN(dashStyleIndex, dataIndex):
    return (BOOLEAN, dash, gap)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dashStyleIndex|LONGINT|The negative value of the dash pattern's internal index.|
|dataIndex|INTEGER|Index of the data value pair.|
|dash|REAL|The dash segement value.|
|gap|REAL|The gap segment value.|

## Examples
```pascal
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
[GetNumDashDataPairsN](GetNumDashDataPairsN.md) 
| [GetDashStyleIndexN](GetDashStyleIndexN.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
