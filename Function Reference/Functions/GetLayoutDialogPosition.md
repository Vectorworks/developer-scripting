# GetLayoutDialogPosition

## Description
This function will retrieve the screen location of the dialog window, in pixels.

This function can be useful for displaying a dialog in a position in which it was placed during prior use.

```pascal
FUNCTION GetLayoutDialogPosition(
				dialogID   : LONGINT;
				VAR left   : INTEGER;
				VAR top    : INTEGER;
				VAR right  : INTEGER;
				VAR bottom : INTEGER): BOOLEAN;
```

```python
def vs.GetLayoutDialogPosition(dialogID):
    return (BOOLEAN, left, top, right, bottom)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index of the dialog.|
|left|INTEGER|Location of left edge of dialog, in pixels.|
|top|INTEGER|Location of top of dialog, in pixels.|
|right|INTEGER|Location of right edge of dialog, in pixels.|
|bottom|INTEGER|Location of bottom edge of dialog, in pixels.|

## Examples
```pascal
BEGIN
	boo := GetLayoutDialogPosition(dialogID, left, top, right, bottom);
	IF left < 1 THEN left := 1;
	IF top < 1 THEN top := 1;
	GetLayoutDialogSize(dialogID, wdth, hght);
	SetSavedSetting('DialogPositions', Concat(dialogName, '/left'), Int2Str(left));

BEGIN
	boo := GetLayoutDialogPosition( dialogID, SettingDlgPos_Left, SettingDlgPos_Top, DumbPosRight, DumbPosBottom );
	SetRField( GetObject( kpioCMObjName ), kpioCMObjName, 'SettingDlgPos_Left', Num2Str( 0, SettingDlgPos_Left ) );
	SetRField( GetObject( kpioCMObjName ), kpioCMObjName, 'SettingDlgPos_Top', Num2Str( 0, SettingDlgPos_Top ) );
END;

BEGIN
	boo := GetLayoutDialogPosition( dialogID, TuneDlgPos_Left, TuneDlgPos_Top, DumbPosRight, DumbPosBottom );
	SetRField( GetObject( kpioCMObjName ), kpioCMObjName, 'TuneDlgPos_Left', Num2Str( 0, TuneDlgPos_Left ) );
	SetRField( GetObject( kpioCMObjName ), kpioCMObjName, 'TuneDlgPos_Top', Num2Str( 0, TuneDlgPos_Top ) );
END;
```
```python
import vs

# This function will retrieve the screen location of the dialog window, in
# pixels.
dialogID = 1

ok, left, top, right, bottom = vs.GetLayoutDialogPosition(dialogID)
vs.Message('GetLayoutDialogPosition returned: ' + str((ok, left, top, right, bottom)))
```

## See Also
VS Functions:
[SetLayoutDialogPosition](SetLayoutDialogPosition.md)

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
