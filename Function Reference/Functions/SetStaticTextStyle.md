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

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
