# SetStaticTextStyle

## Description
Sets the style for the Layout Manager static Text<BR>
<BR>
Plain 0<BR>
Bold 1<BR>
Italic 2<BR>
Underline 4<BR>
<BR>
Can combine styles (bold + italic = 3)

```pascal
PROCEDURE SetStaticTextStyle(
				dialogID    : LONGINT;
				componentID : LONGINT;
				style       : INTEGER);
```

```python
def vs.SetStaticTextStyle(dialogID, componentID, style):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|style|INTEGER|   |

## Examples
```pascal
SetStaticTextStyle(dialog1, kStaticText13, 1);

BEGIN
	CreateStaticText( DialogID, kMsgLblStaTex_ID, '//// Debug Message:', -1 );
	SetBelowItem( DialogID, kPreviewGroup_ID, kMsgLblStaTex_ID, 0, 0 );
	SetStaticTextColor( DialogID, kMsgLblStaTex_ID, StaTexRed_R, StaTexRed_G, StaTexRed_B );
	SetStaticTextStyle( DialogID, kMsgLblStaTex_ID, 1 );	{set style to bold}

SetStaticTextStyle( dialog, kTypeHeader, 1 );
```
```python
import vs

# Sets the style for the Layout Manager static Text Plain 0 Bold 1 Italic 2
# Underline 4 Can combine styles (bold + italic = 3).
dialogID = 1
componentID = 2
style = 0

vs.SetStaticTextStyle(dialogID, componentID, style)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
