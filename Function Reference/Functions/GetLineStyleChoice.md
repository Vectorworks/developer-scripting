# GetLineStyleChoice

## Description
Get current choice of line style popup dialog control.  Choice is an index into list of linestyles available in current document.

```pascal
PROCEDURE GetLineStyleChoice(
				dialogID      : LONGINT;
				itemID        : LONGINT;
				VAR lineStyle : INTEGER);
```

```python
def vs.GetLineStyleChoice(dialogID, itemID):
    return lineStyle
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|lineStyle|INTEGER|   |

## Remarks
Get current choice of line style popup dialog control.  Choice is an index into list of linestyles available in current document.

*_c_* (2016.02.29): Returns a dash list index (not usable with VS:Index2Name).

## Version
Availability: from VectorWorks 12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
