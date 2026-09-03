# CreateSeparator

## Description
Creates a Layout Manager image separator.

```pascal
PROCEDURE CreateSeparator(
				dialogID    : LONGINT;
				componentID : LONGINT;
				iLength     : INTEGER);
```

```python
def vs.CreateSeparator(dialogID, componentID, iLength):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|iLength|INTEGER|   |

## Examples
```pascal
CreateCheckBox      (dialog1, kCheckBox10,   GetStr(kCheckBox10));
CreateStaticText    (dialog1, kStaticText11,  GetStr(kStaticText11), -1);
CreateEditReal      (dialog1, kEditReal12,    3, 0.0, 20);
CreateStaticText    (dialog1, kStaticText13,  gLocPluginName, 25);
CreateSeparator     (dialog1, kStaticText14, -1);
CreateCheckBox		(dialog1, kCheckBox30,	 GetStr(kCheckBox30));

CreatePulldownMenu(dialogID3, 6, 17);
CreateRadioButton (dialogID3, 7, GetPlugInString(7007));
CreateCheckBox    (dialogID3, 8, GetPlugInString(7008));
CreateStaticText  (dialogID3, 9, GetPlugInString(7009), -1);
CreateSeparator	  (dialogID3, 10,30);
CreateStaticText  (dialogID3, 11, GetPlugInString(7011), -1);
CreateEditText    (dialogID3, 12, GetPlugInString(7012), 7);
CreateStaticText  (dialogID3, 13, GetPlugInString(13011), -1);
CreateStaticText  (dialogID3, 14, GetPlugInString(7014), -1);

CreateCheckBox( dialog, 	kBmpTiltChkBx, 		GetStr(kBmpTiltChkBx) );
CreateCheckBox( dialog, 	kBmpTrimChkBx, 		GetStr(kBmpTrimChkBx) );
CreateCheckBox( dialog, 	kBtmBxTrimChkBx, 	GetStr(kBtmBxTrimChkBx) );
CreateCheckBox( dialog, 	kNotesChkBx, 		GetStr(kNotesChkBx) );
CreateSeparator( dialog,	kSeparator,			0 );
CreateCheckBox( dialog, 	kRoundDimsChkBx, 	GetStr(kRoundDimsChkBx) );
CreateCheckBox( dialog, 	kInclTxtLabChkBx,	GetStr(kInclTxtLabChkBx) );
CreateGroupBox( dialog, 	kTxtAttrsBx, 		GetStr(kTxtAttrsBx), TRUE );
CreateCheckBox( dialog, 	kTextHorizChkBx,	GetStr(kTextHorizChkBx) );
```
```python
import vs

# Creates a Layout Manager image separator.
dialogID = 1
componentID = 2
iLength = 3

vs.CreateSeparator(dialogID, componentID, iLength)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
