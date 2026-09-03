# CreateColorPopup

## Description
Create a color popup dialog control that displays the 256 color palette associated with the active document.  

The widthInCharacters argument specifies the width of the control.  Pass -1 to request the default size, which will be consistent with other attribute controls (currently defaults to 14).  This argument allows for special circumstances like a small popup for the Fore and Back color associated with the Pattern attribute control.

```pascal
PROCEDURE CreateColorPopup(
				dialogID          : LONGINT;
				itemID            : LONGINT;
				widthInCharacters : LONGINT);
```

```python
def vs.CreateColorPopup(dialogID, itemID, widthInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|widthInCharacters|LONGINT|   |

## Examples
[ColorPopupDialog](examples/ColorPopupDialog.md)

```pascal
CreateGroupBox  ( dialogID, kSecondGroupBox, '', True);
CreateStaticText( dialogID, kstColor, GetStr2(kstColor),  -1 );
   if isMac then
     CreateColorPopup( dialogID, kColorPopupID , 26)
   else
     CreateColorPopup( dialogID, kColorPopupID , 20 );
SetHelpText(dialogID, kColorPopupID, GetHelpStr(1));

CreateColorPopup(dialogID, 25, kColorWidth);			{pen color}
CreateLineWeightPopup(dialogID, 26);				{line weight}
CreateLineStylePopup(dialogID, 27);					{line style}
CreatePatternPopup(dialogID, 28);					{fill pattern}
CreateColorPopup(dialogID, 29, kForeBackColorWidth);		{fill fore color}

   CreateEditText( dialog, kSymNameEdit, GetStr(kSymNameEdit), 20 );
   CreateStaticText( dialog, kClassNameLab, GetStr(kClassNameLab), -1 );
   CreateClassPullDownMenu( dialog, kClassNamePop, 20 );
   CreateStaticText( dialog, kFillColorLab, GetStr(kFillColorLab), -1 );
   CreateColorPopup( dialog, kFillColorPop, 16 );
   CreateStaticText( dialog, klFloorPen, GetStr(klFloorPen), -1 );
   CreateColorPopup( dialog, kPenColorPop, 16 );
   CreateStaticText( dialog, kTextureLab, GetStr(kTextureLab), -1 );
{   CreateControl( dialog, kTexturePop, 10, '', 0); }
```
```python
import vs

# Create a color popup dialog control that displays the 256 color palette
# associated with the active document.
dialogID = 1
itemID = 2
widthInCharacters = 3

vs.CreateColorPopup(dialogID, itemID, widthInCharacters)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
