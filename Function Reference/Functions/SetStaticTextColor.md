# SetStaticTextColor

## Description
Sets the color for the Layout Manager static Text

```pascal
PROCEDURE SetStaticTextColor(
				dialogID    : LONGINT;
				componentID : LONGINT;
				red         : INTEGER;
				green       : INTEGER;
				blue        : INTEGER);
```

```python
def vs.SetStaticTextColor(dialogID, componentID, red, green, blue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|red|INTEGER|   |
|green|INTEGER|   |
|blue|INTEGER|   |

## Remarks
\_c\_, (2021.01.03): This is broken on VW 2020 and 2021: the text stays black, unregarded the color setting passed.

\_c\_, (2014.04.27):  This only works during [ dialog setup](CreateResizableLayout.md), the color cannot be changed later, for example during event [[VS:Creating_a_Custom_Dialog_Box| SetupDialogC]].

## Examples
```pascal
CreateStyledStatic( dialogID, RefObjInfoStaTex1_ID, dlogSetStaTex_5, -1, 0 {111} );
	SetStaticTextColor( dialogID, RefObjInfoStaTex1_ID, StaTexBlue_R, StaTexBlue_G, StaTexBlue_B );
SetBelowItem( dialogID, ReferenceObjStaTex_ID, RefObjInfoStaTex1_ID, 0, -2 );

BEGIN
	CreateStaticText( DialogID, kMsgLblStaTex_ID, '//// Debug Message:', -1 );
	SetBelowItem( DialogID, kPreviewGroup_ID, kMsgLblStaTex_ID, 0, 0 );
	SetStaticTextColor( DialogID, kMsgLblStaTex_ID, StaTexRed_R, StaTexRed_G, StaTexRed_B );
	SetStaticTextStyle( DialogID, kMsgLblStaTex_ID, 1 );	{set style to bold}
```
```python
import vs

# Sets the color for the Layout Manager static Text.
dialogID = 1
componentID = 2
red = 65535
green = 0
blue = 0

vs.SetStaticTextColor(dialogID, componentID, red, green, blue)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
