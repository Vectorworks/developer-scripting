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

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
