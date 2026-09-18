# SetClLSN

## Description
Sets the line style of the specified class.

```pascal
PROCEDURE SetClLSN(
				className : STRING;
				lineStyle : LONGINT);
```

```python
def vs.SetClLSN(className, lineStyle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|lineStyle|LONGINT|Line style index value.|

## Examples
```pascal
GetWSCellValue (wksHand, row, col+3, tempLong);	{line style}
SetClLSN (userClassName, tempLong);

IF GetClLSN (UserClassName) <> TmpClassInfo.LS THEN SetClLSN (UserClassName, TmpClassInfo.LS);

BEGIN
	NameClass (UserClassName);
	SetClPenFore (UserClassName, DecimalToColorIndex(TmpClassInfo.PenColor));
	SetClLW (UserClassName, TmpClassInfo.LW);
	SetClLSN (UserClassName, TmpClassInfo.LS);
	SetClFPat (UserClassName, TmpClassInfo.FillPat);
	SetClFillFore (UserClassName, DecimalToColorIndex (TmpClassInfo.FillFore));
	SetClFillBack (UserClassName, DecimalToColorIndex (TmpClassInfo.FillBack));
	SetClUseGraphic (UserClassName, TmpClassInfo.UseAtCreation);
```
```python
vs.SetClLW( userClassName, tempInt )
tempInt = vs.GetWSCellValue( wksHand, row, col + 3 )
# line style
vs.SetClLSN( userClassName, tempInt )
tempInt = vs.GetWSCellValue( wksHand, row, col + 4 )
# fill pattern
vs.SetClFPat( userClassName, tempInt )
tempInt = vs.GetWSCellValue( wksHand, row, col + 5 )
```

## See Also
VS Functions:
[GetClLSN](GetClLSN.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Classes](../Categories/Classes.md)
