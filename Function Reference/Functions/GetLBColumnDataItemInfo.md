# GetLBColumnDataItemInfo

## Description
Gets the specified column data item's text, image and user data.

```pascal
FUNCTION GetLBColumnDataItemInfo(
				dialogID            : LONGINT;
				componentID         : LONGINT;
				columnIndex         : INTEGER;
				columnDataItemIndex : INTEGER;
				VAR itemString      : STRING;
				VAR imageOn         : INTEGER;
				VAR imageOff        : INTEGER;
				VAR itemData        : LONGINT): BOOLEAN;
```

```python
def vs.GetLBColumnDataItemInfo(dialogID, componentID, columnIndex, columnDataItemIndex):
    return (BOOLEAN, itemString, imageOn, imageOff, itemData)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column from which to get the data|
|columnDataItemIndex|INTEGER|the column data item|
|itemString|STRING|the item text|
|imageOn|INTEGER|the 'on' image list index|
|imageOff|INTEGER|the 'off' image list index|
|itemData|LONGINT|the item user data|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
