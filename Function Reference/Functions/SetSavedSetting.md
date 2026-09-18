# SetSavedSetting

## Description
Writes a value to the saved settings file.  This can be used to remember various user settings between running sessions of VectorWorks.  For example, a script may want to remember a dialog's position or a font settings.  The saved settings should not be used for critical information, but rather for convenience settings.

```pascal
PROCEDURE SetSavedSetting(
				category : STRING;
				setting  : STRING;
				value    : STRING);
```

```python
def vs.SetSavedSetting(category, setting, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|category|STRING|   |
|setting|STRING|   |
|value|STRING|   |

## Remarks
This stores the data on SavedSettingsUser.xml. 
If the file SavedSettingsUser.xml is missing, it will be created in the users&gt;Settings folder AFTER quitting VectorWorks and only if the file calling this routine is saved (VW 12.x).

This seems to mean that the whole xml is stored on memory as long as the VW session is open. It will be written and released after quitting the application. Not clear as to what happens if you keep on calling this routine from a large number of scripts, on a large number of open files, using a large number of different setting values.

## Examples
```pascal
BEGIN
	SetSavedSetting('IDLabelTool','AutoIncrement',Boo2Str(gIDAutoInc));
END;

SetSavedSetting('RevisionCloud','Mode1',Concat(modeValue_1));
SetSavedSetting('RevisionCloud','Mode2',Concat(modeValue_2));

	boo := GetLayoutDialogPosition(dialogID, left, top, right, bottom);
	IF left < 1 THEN left := 1;
	IF top < 1 THEN top := 1;
	GetLayoutDialogSize(dialogID, wdth, hght);
	SetSavedSetting('DialogPositions', Concat(dialogName, '/left'), Int2Str(left));
	SetSavedSetting('DialogPositions', Concat(dialogName, '/top'), Int2Str(top));
	SetSavedSetting('DialogPositions', Concat(dialogName, '/wdth'), Int2Str(wdth));
	SetSavedSetting('DialogPositions', Concat(dialogName, '/hght'), Int2Str(hght));
END;
```
```python
import vs

# Writes a value to the saved settings file.
category = 'Example'
setting = 'Example'
value = 'Example'

vs.SetSavedSetting(category, setting, value)
```

## See Also
[GetSavedSetting](GetSavedSetting.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Utility](../Categories/Utility.md)
