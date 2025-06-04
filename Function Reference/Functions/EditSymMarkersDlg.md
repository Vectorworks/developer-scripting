# EditSymMarkersDlg

## Description
Function EditSymMarkersDlg displays a dialog box which requests the user to choose starting and ending symbol markers. Returns TRUE if OK is clicked. Parameters inOutStartMarkerSymName and inOutEndMarkerSymName set the symbols to initialize selected symbols and return the newly selected symbol names.

```pascal
FUNCTION EditSymMarkersDlg(
				dialogTitle                 : STRING;
				contextHelpID               : STRING;
				VAR inOutStartMarkerSymName : STRING;
				VAR inOutEndMarkerSymName   : STRING): BOOLEAN;
```

```python
def vs.EditSymMarkersDlg(dialogTitle, contextHelpID, inOutStartMarkerSymName, inOutEndMarkerSymName):
    return (BOOLEAN, inOutStartMarkerSymName, inOutEndMarkerSymName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogTitle|STRING|Dialog title string.|
|contextHelpID|STRING|Contextual help ID string.|
|inOutStartMarkerSymName|STRING|Name of starting symbol marker.|
|inOutEndMarkerSymName|STRING|Name of ending symbol marker.|

## Version
Availability: from Vectorworks 2020

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
