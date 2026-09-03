# SetClLW

## Description
Sets the line weight of the specified class.

```pascal
PROCEDURE SetClLW(
				className : STRING;
				LW        : INTEGER);
```

```python
def vs.SetClLW(className, LW):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|LW|INTEGER|Line weight value (in mils).|

## Remarks
Assigns the specified line style to the class named className.

## Examples
#### VectorScript ####
```pascal
SetClLW('To Be Demolished',28);
```
#### Python ####
```python

```

```pascal
GetWSCellValue (wksHand, row, col+2, tempInt);	{line weight}
SetClLW (userClassName, tempInt);

IF GetClLW (UserClassName) <> TmpClassInfo.LW THEN SetClLW (UserClassName, TmpClassInfo.LW);

BEGIN
	NameClass (UserClassName);
	SetClPenFore (UserClassName, DecimalToColorIndex(TmpClassInfo.PenColor));
	SetClLW (UserClassName, TmpClassInfo.LW);
	SetClLSN (UserClassName, TmpClassInfo.LS);
	SetClFPat (UserClassName, TmpClassInfo.FillPat);
	SetClFillFore (UserClassName, DecimalToColorIndex (TmpClassInfo.FillFore));
	SetClFillBack (UserClassName, DecimalToColorIndex (TmpClassInfo.FillBack));
```
```python
vs.SetClPenFore( userClassName, r, g, b )
tempInt = vs.GetWSCellValue( wksHand, row, col + 2 )
# line weight
vs.SetClLW( userClassName, tempInt )
tempInt = vs.GetWSCellValue( wksHand, row, col + 3 )
# line style
vs.SetClLSN( userClassName, tempInt )
tempInt = vs.GetWSCellValue( wksHand, row, col + 4 )
```
See also in tutorials: [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
