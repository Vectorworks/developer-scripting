# SetLBItemDashStyle

## Description
Sets the specified list browser item's dash style.

```pascal
FUNCTION SetLBItemDashStyle(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				styleIndex   : INTEGER;
				lineWeight   : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemDashStyle(dialogID, componentID, itemIndex, subItemIndex, styleIndex, lineWeight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|styleIndex|INTEGER|the dash line's style index|
|lineWeight|INTEGER|the dash line's line weight|

## Remarks
[[User:CBM-c-|_c_]] (2016.02.29): Expects a dash list index (not from the name list).

## Version
Availability: from VectorWorks 12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
