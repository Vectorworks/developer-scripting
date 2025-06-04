# GetPatternData

## Description
Get current choice for pattern popup dialog control, and the displayed foreground and background color indexes.

```pascal
PROCEDURE GetPatternData(
				dialogID         : LONGINT;
				itemID           : LONGINT;
				VAR patternIndex : INTEGER;
				VAR foreColor    : INTEGER;
				VAR backColor    : INTEGER);
```

```python
def vs.GetPatternData(dialogID, itemID):
    return (patternIndex, foreColor, backColor)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|patternIndex|INTEGER|   |
|foreColor|INTEGER|   |
|backColor|INTEGER|   |

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
