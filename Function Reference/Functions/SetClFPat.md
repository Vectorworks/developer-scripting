# SetClFPat

## Description
Sets the fill pattern of the specified class.

To apply a bitmap fill pattern, use a positive value corresponding to the desired fill pattern index. To apply a vector fill, use the negative of the index of the vector fill (index * -1).

Fill patterns and their associated constants can be found in the [VectorScript Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
PROCEDURE SetClFPat(
				className   : STRING;
				fillpattern : LONGINT);
```

```python
def vs.SetClFPat(className, fillpattern):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|fillpattern|LONGINT|Fill pattern index value.|

## Remarks
Assigns a fill pattern to the class named className.

## Examples
#### VectorScript ####
```pascal
SetClFPat('Grassy Cover',42);
```
#### Python ####
```python

```

```pascal
GetWSCellValue (wksHand, row, col+4, tempInt);	{fill pattern}
SetClFPat (userClassName, tempInt);

IF GetClFPat (UserClassName) <> TmpClassInfo.FillPat THEN SetClFPat (UserClassName, TmpClassInfo.FillPat);

NameClass (UserClassName);
SetClPenFore (UserClassName, DecimalToColorIndex(TmpClassInfo.PenColor));
SetClLW (UserClassName, TmpClassInfo.LW);
SetClLSN (UserClassName, TmpClassInfo.LS);
SetClFPat (UserClassName, TmpClassInfo.FillPat);
SetClFillFore (UserClassName, DecimalToColorIndex (TmpClassInfo.FillFore));
SetClFillBack (UserClassName, DecimalToColorIndex (TmpClassInfo.FillBack));
SetClUseGraphic (UserClassName, TmpClassInfo.UseAtCreation);
tempH := GetObject (UserClassName);
```
```python
vs.SetClLSN( userClassName, tempInt )
tempInt = vs.GetWSCellValue( wksHand, row, col + 4 )
# fill pattern
vs.SetClFPat( userClassName, tempInt )
tempInt = vs.GetWSCellValue( wksHand, row, col + 5 )
# fill fore pen color
r, g, b = vs.ColorIndexToRGB( tempInt, r, g, b )
vs.SetClFillFore( userClassName, r, g, b )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
