# SetLBItemLineType

## Description
Sets the specified list browser item's line type.

```pascal
FUNCTION SetLBItemLineType(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				lineType     : LONGINT;
				lineWeight   : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemLineType(dialogID, componentID, itemIndex, subItemIndex, lineType, lineWeight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|lineType|LONGINT|the line type internal index (reference number)|
|lineWeight|INTEGER|the line weight|

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
