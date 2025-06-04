# GetLBItemOrigName

## Description
Returns the original name for a list browser item when hierarchical display is on. If the item is a container item, it will return an empty string.

```pascal
FUNCTION GetLBItemOrigName(
				dialogID    : LONGINT;
				compenentID : LONGINT;
				itemIndex   : INTEGER): STRING;
```

```python
def vs.GetLBItemOrigName(dialogID, compenentID, itemIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog.|
|compenentID|LONGINT|The id of the list browser.|
|itemIndex|INTEGER|The index of the item for which the original name is returned.|

## See Also
VS Functions:
[AddLBOriginalName](AddLBOriginalName.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
