# GetLBItemDashStyle

## Description
Gets the specified list browser item's dash style.

```pascal
FUNCTION GetLBItemDashStyle(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				VAR styleIndex : INTEGER;
				VAR lineWeight : INTEGER): BOOLEAN;
```

```python
def vs.GetLBItemDashStyle(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, styleIndex, lineWeight)
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

## Examples
```pascal
resultOK := GetLBItemDashStyle(1, 2, 3, 10, 5, 1);
```
```python
import vs

# Gets the specified list browser item's dash style.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1

ok, styleIndex, lineWeight = vs.GetLBItemDashStyle(dialogID, componentID, itemIndex, subItemIndex)
vs.Message('GetLBItemDashStyle returned: ' + str((ok, styleIndex, lineWeight)))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
