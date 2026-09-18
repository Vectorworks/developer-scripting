# SetControlText

## Description
Sets the text of radio button, check box, push button controls.

```pascal
PROCEDURE SetControlText(
				DlogID  : INTEGER;
				ItemID  : INTEGER;
				newtext : STRING);
```

```python
def vs.SetControlText(DlogID, ItemID, newtext):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|DlogID|INTEGER|ID of the dialog|
|ItemID|INTEGER|ID of the control|
|newtext|STRING|Text to insert|

## Examples
```pascal
	dummy_i := InsertImagePopupObjectItem(dialog1,5, getrfield(unique_plants[i],'Plant','plantDescription'));
	END;
SelectChoice(dialog1, 4,0,TRUE);
SetImagePopupSelectedItem(dialog1,5,1);
SetControlText(dialog1, 8, num2strf(str2num(getrfield(unique_plants[1],'Plant','spread'))));
END;

defH:=GetObject(GetImagePopupObject(SDDialog_ID, 11, choiceInt));
IF defH<>NIL THEN BEGIN
	IF GetType(defH)=kSymbolFolderType THEN BEGIN
		EnableItem(SDDialog_ID, 12, TRUE);
		SetControlText(SDDialog_ID, 1, 'Open');
	END
```
```python
import vs

# Sets the text of radio button, check box, push button controls.
DlogID = 1
ItemID = 2
newtext = 'Example text'

vs.SetControlText(DlogID, ItemID, newtext)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
