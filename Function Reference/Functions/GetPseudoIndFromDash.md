# GetPseudoIndFromDash

## Description
Supplies a pseudo index for a dashed style. The returned index is not guaranteed to produce the same line type from file to file, nor even in the same file if line types change.<BR>
Returns TRUE if successful.

```pascal
FUNCTION GetPseudoIndFromDash(
				dashStyle          : LONGINT;
				VAR outPseudoIndex : INTEGER): BOOLEAN;
```

```python
def vs.GetPseudoIndFromDash(dashStyle):
    return (BOOLEAN, outPseudoIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dashStyle|LONGINT|Negative internal index of a dashed line type.|
|outPseudoIndex|INTEGER|Pseudo index (a negative number) corresponding to the dash style.  The psuedo index is not guaranteed to produce the same line across files (or even in the same file if line types are changed).|

## Examples
```pascal
BEGIN
	convertResult := GetPseudoIndFromDash(lineStyle, result);
	IF NOT convertResult THEN result := 2;
	ConvertDashToPseudoInd := result;
END;

BEGIN
	colorIndex := decimalToColorIndex (gClassList [i].PenColor);
	SetWSCellFormula (gClassWSHandle, 1+i, col+1, 1+i, col+1, Num2Str (0, colorIndex));
	SetWSCellFormula (gClassWSHandle, 1+i, col+2, 1+i, col+2, Num2Str (0, gClassList [i].LW));
	convertStatus := GetPseudoIndFromDash (gClassList [i].LS, pseudoIndex);
	SetWSCellFormula (gClassWSHandle, 1+i, col+3, 1+i, col+3, Num2Str (0, pseudoIndex));
	SetWSCellFormula (gClassWSHandle, 1+i, col+4, 1+i, col+4, Num2Str (0, gClassList [i].FillPat));
	colorIndex := decimalToColorIndex (gClassList [i].FillFore);
	SetWSCellFormula (gClassWSHandle, 1+i, col+5, 1+i, col+5, Num2Str (0, colorIndex));

SetRField( GetObject( kpioCMObjName ), kpioCMObjName, 'PhotoBrightness', Num2Str( 0, pioPhotoBrightness ) );
SetRField( GetObject( kpioCMObjName ), kpioCMObjName, 'PhotoImageResource', pioPhotoRsrcName );
SetRField( GetObject( kpioCMObjName ), kpioCMObjName, 'RenderBackground', pioRWBackRsrcName );
SetRField( GetObject( kpioCMObjName ), kpioCMObjName, 'RefModelName', RefGridPIOName );
convertRes := GetPseudoIndFromDash(pioMeasureLineStyle, pseudoInd);
IF NOT convertRes THEN
	pseudoInd := 2;  {solid line}
SetRField( GetObject( kpioCMObjName ), kpioCMObjName, 'MeasureLineStyle', Num2Str( 0, pseudoInd) );
```
```python
import vs

# Supplies a pseudo index for a dashed style.
dashStyle = 0

ok, outPseudoIndex = vs.GetPseudoIndFromDash(dashStyle)
vs.Message('GetPseudoIndFromDash returned: ' + str((ok, outPseudoIndex)))
```

## See Also
VS Functions:
[GetDashFromPseudoInd](GetDashFromPseudoInd.md) 
| [BeginMultDashConvert](BeginMultDashConvert.md) 
| [EndMultDashConvert](EndMultDashConvert.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Utility](../Categories/Utility.md)
