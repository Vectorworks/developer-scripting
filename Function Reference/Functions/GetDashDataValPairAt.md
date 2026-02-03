# GetDashDataValPairAt

## Description
Function GetDashDataValPairAt gets the dash data for the specified dash style. The dash data is a dash/gap value pair. GetDashDataValPairAt returns false if the dash style or dash data doesn't exist. Dash styles support up to 5 dash/gap value pairs.

```pascal
FUNCTION GetDashDataValPairAt(
				dashStyleIndex : INTEGER;
				dataIndex      : INTEGER;
				VAR dash       : REAL;
				VAR gap        : REAL): BOOLEAN;
```

```python
def vs.GetDashDataValPairAt(dashStyleIndex, dataIndex):
    return (BOOLEAN, dash, gap)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dashStyleIndex|INTEGER|The dash style index.|
|dataIndex|INTEGER|Index fo the data value pair.|
|dash|REAL|The dash segement value.|
|gap|REAL|The gap segment value.|

## Remarks
*\_c\_*, 2016.03.01:
* The dash style index required is relative to the dash style list, not the name list. Use [GetDashStyle](GetDashStyle.md) or [GetDashStyleIndex](GetDashStyleIndex.md) to obtain it.
* The count of dash/gap pairs and the boolean value swt (if scale with thickness is ON) can be fetched with [GetNumDashDataPairs](GetNumDashDataPairs.md). 
* The REAL values returned are page inches.

## Examples
```pascal
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
[GetNumDashDataPairs](GetNumDashDataPairs.md) 
| [GetDashStyleIndex](GetDashStyleIndex.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
