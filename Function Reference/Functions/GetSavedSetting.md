# GetSavedSetting

## Description
Reads a value from the saved settnigs file.  This can be used to remember various user settings between running sessions of VectorWorks.  For example, a script may want to remember a dialog's position or a font settings.  The saved settings should not be used for critical information, but rather for convenience settings. 

If the settings file is lost or damaged the script should revert to a reasonable default value, and typically this would not warrant an alert dialog.

```pascal
FUNCTION GetSavedSetting(
				category  : STRING;
				setting   : STRING;
				VAR value : STRING): BOOLEAN;
```

```python
def vs.GetSavedSetting(category, setting):
    return (BOOLEAN, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|category|STRING|   |
|setting|STRING|   |
|value|STRING|   |

## Remarks
This routine operates on XML memory.
It also access the file SavedSettingsUser.xml in the User's &gt; setting folder, should that be available. See SetSavedSetting for more info.

The script below illustrates how it works. Open the "Settings" folder in your user's folder, move out the file SavedSettingsUser.xml, should you have it there already. Then launch the script below some times, save file and quit application.
If you didn't have the file SavedSettingsUser.xml there, one such file will be created after quitting VW. But you'll notice that the values returned in the dialog are always increasing every time the script runs.
From memory. The file wasn't there while you runned it.
```pascal
PROCEDURE Example;
VAR
incremented : INTEGER;
temp_s      : STRING;
temp_b      : BOOLEAN;

BEGIN
temp_b := GetSavedSetting('Bombarder', 'BOMB', temp_s);
IF NOT ValidNumStr(temp_s, incremented) THEN BEGIN
incremented := 1;
END ELSE BEGIN
incremented := incremented + 1;
END;
SetSavedSetting('Bombarder', 'BOMB', Concat(incremented));
AlrtDialog(Concat(incremented));
END;
RUN(Example);
```

## See Also
VS:SetSavedSetting

## Version
Availability: from VectorWorks12.0

## Category
* [Utility](../Categories/Utility.md)
