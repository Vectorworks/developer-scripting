# CreateClassPullDownMenu

## Description
Creates a Layout Manager class pull down menu control.

```pascal
PROCEDURE CreateClassPullDownMenu(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nWidthInChars : INTEGER);
```

```python
def vs.CreateClassPullDownMenu(nDialogID, nComponentID, nWidthInChars):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nWidthInChars|INTEGER|   |

## Remarks
*\_c\_* (2016.02.22): Add the localized string "<Object Class>" below "New...". You must do this during the SetupDialogC event of your dialog driver:
<code lang="vs">
GetResourceString(objClassString, 2103, 148); { fetches the localized "<Object Class>" string }
IF InsertPropClassOrLayerItem(dialogID, c_classPullDownMenu_Index, objClassString, '') THEN
	{ do something, eventually };
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
	dialog1 :INTEGER;
	result  :INTEGER;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
	BEGIN
	END;
BEGIN
	dialog1 := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
	CreateClassPullDownMenu(dialog1, 4, 24);
	SetFirstLayoutItem(dialog1, 4);
	result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
#### Python ####
```python
def Dialog_Handler(item , data ):
	pass
def Example():
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	vs.CreateClassPullDownMenu(dialog1, 4, 24)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)

Example()
```

## See Also
VS Functions:
[CreateImageControl](CreateImageControl.md), 
[InsertPropClassOrLayerItem](InsertPropClassOrLayerItem.md)

## Version
Availability: from VectorWorks 13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
