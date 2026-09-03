# GetDashFromPseudoInd

## Description
Gets the dash style that corresponds to the pseudo index and returns the style's internal index. Returns TRUE if successful.<BR>
<BR>

```pascal
FUNCTION GetDashFromPseudoInd(
				pseudoIndex      : INTEGER;
				VAR outDashStyle : LONGINT): BOOLEAN;
```

```python
def vs.GetDashFromPseudoInd(pseudoIndex):
    return (BOOLEAN, outDashStyle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pseudoIndex|INTEGER|Pseudo index (negative value)  for which a dash style is requested.|
|outDashStyle|LONGINT|Negative internal index of a dashed line type corresponding to the psuedo index.|

## Examples
```pascal
BEGIN
	convertResult := GetDashFromPseudoInd(pseudoIndex, result);
	IF NOT convertResult THEN result := 2;
	ConvertPseudoIndToDash := result;
END;

GetWSCellValue (gClassWSHandle, 1+i, col+1, colorIndex);
gClassList [i].PenColor := colorIndexToDecimal (colorIndex);
GetWSCellValue (gClassWSHandle, 1+i, col+2, gClassList [i].LW);
GetWSCellValue (gClassWSHandle, 1+i, col+3, pseudoIndex);
convertStatus := GetDashFromPseudoInd(pseudoIndex, gClassList [i].LS);
GetWSCellValue (gClassWSHandle, 1+i, col+4, gClassList [i].FillPat);
GetWSCellValue (gClassWSHandle, 1+i, col+5, colorIndex);
gClassList [i].FillFore := colorIndexToDecimal (colorIndex);
GetWSCellValue (gClassWSHandle, 1+i, col+6, colorIndex);

BEGIN
	convertRes := GetDashFromPseudoInd(Str2Num( GetRField( PIOHand, GetName(PIORecHand), 'MeasureLineStyle' ) ), lineStyle);
	IF NOT convertRes
	THEN
	BEGIN
		lineStyle := CheckLSN(-1); {set to basic dash line if valid value not found}
```
```python
import vs

# Gets the dash style that corresponds to the pseudo index and returns the
# style's internal index.
pseudoIndex = 1

ok, outDashStyle = vs.GetDashFromPseudoInd(pseudoIndex)
vs.Message('GetDashFromPseudoInd returned: ' + str((ok, outDashStyle)))
```

## See Also
VS Functions:
[GetPseudoIndFromDash](GetPseudoIndFromDash.md) 
| [BeginMultDashConvert](BeginMultDashConvert.md) 
| [EndMultDashConvert](EndMultDashConvert.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Utility](../Categories/Utility.md)
