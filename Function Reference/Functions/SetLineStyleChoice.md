# SetLineStyleChoice

## Description
Set the current choice of the line style popup dialog control to the specified index.

```pascal
PROCEDURE SetLineStyleChoice(
				dialogID  : LONGINT;
				itemID    : LONGINT;
				lineStyle : INTEGER);
```

```python
def vs.SetLineStyleChoice(dialogID, itemID, lineStyle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|lineStyle|INTEGER|   |

## Remarks
Set the current choice of the line style popup dialog control to the specified index.

\_c\_ (2016.02.29): Expects a dash list index (not usable for VS:Index2Name).

## Version
Availability: from VectorWorks 12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
