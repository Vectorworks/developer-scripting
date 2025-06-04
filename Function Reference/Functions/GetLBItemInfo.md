# GetLBItemInfo

## Description
Gets string and image information for a specified item of a List Browser control.

```pascal
FUNCTION GetLBItemInfo(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				VAR itemString : STRING;
				VAR imageIndex : INTEGER): BOOLEAN;
```

```python
def vs.GetLBItemInfo(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, itemString, imageIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the item index|
|subItemIndex|INTEGER|the subitem index|
|itemString|STRING|the item text|
|imageIndex|INTEGER|the item image list index|

## Remarks
&lt;li&gt;itemIndex = row
&lt;li&gt;subItemIndex = column

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
