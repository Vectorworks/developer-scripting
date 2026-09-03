# CreateResizableLayout

## Description
Creates a new resizable Layout Manager dialog.

Resizable dialogs raise the ResizeDialogC event when resized.

```pascal
FUNCTION CreateResizableLayout(
				dialogTitle       : STRING;
				hasHelp           : BOOLEAN;
				defaultButtonName : STRING;
				cancelButtonName  : STRING;
				widthResizable    : BOOLEAN;
				heightResizable   : BOOLEAN): LONGINT;
```

```python
def vs.CreateResizableLayout(dialogTitle, hasHelp, defaultButtonName, cancelButtonName, widthResizable, heightResizable):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogTitle|STRING|   |
|hasHelp|BOOLEAN|   |
|defaultButtonName|STRING|   |
|cancelButtonName|STRING|   |
|widthResizable|BOOLEAN|   |
|heightResizable|BOOLEAN|   |

## Remarks
The parameters are the same as CreateLayout, except for widthResizable and heightResizable, which specify that the width and height, respectively, be resizable.  A dialog ID is returned by the function.

## Examples
```pascal
BEGIN
	dialog1 := CreateResizableLayout(GetStr( 3), TRUE, GetStr(kOK), GetStr(kCancel), TRUE, TRUE);
	CreateStaticText          (dialog1, kStaticText4Shaft,   		GetStr(kStaticText4Shaft), -1);
	CreateClassPullDownMenu   (dialog1, kPopup5ShaftFinish,        	20);
	CreateStaticText          (dialog1, kStaticText6CapitalFinish,  GetStr(kStaticText6CapitalFinish), -1);
	CreateClassPullDownMenu   (dialog1, kPopup5CapitalFinish,       20);

BEGIN
	dialog := CreateResizableLayout( GetLocStr( kListID, kDialogTitle ), TRUE, GetLocStr( kListID, kOK ), GetLocStr( kListID, kCancel ), FALSE, FALSE );

BEGIN
	dialog1 := CreateResizableLayout(GetStr( 3), True, GetStr(kOK), GetStr(kCancel), TRUE, FALSE);
	CreateStaticText          (dialog1, kStaticText4,  GetStr(kStaticText4), -1);
{	CreateControl             (dialog1, kImagePopup5,  10, '', 0); }
    CreateThumbnailPopup(dialog1, kImagePopup5);
	CreateStaticText          (dialog1, kStaticText6,  GetStr(kStaticText6), -1);
```
```python
import vs

# Creates a new resizable Layout Manager dialog.
dialogTitle = 'Example'
hasHelp = True
defaultButtonName = 'Example'
cancelButtonName = 'Example'
widthResizable = True
heightResizable = True

resultN = vs.CreateResizableLayout(dialogTitle, hasHelp, defaultButtonName, cancelButtonName, widthResizable, heightResizable)
vs.Message('CreateResizableLayout returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetEdgeBinding](SetEdgeBinding.md) 
| [SetProportionalBinding](SetProportionalBinding.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
