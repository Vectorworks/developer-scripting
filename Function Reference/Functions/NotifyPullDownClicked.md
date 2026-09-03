# NotifyPullDownClicked

## Description
Sends an item hit notification when the pull down menu is clicked, allowing developers to dynamically populate the menu.

```pascal
PROCEDURE NotifyPullDownClicked(
				nDialogID    : LONGINT;
				nComponentID : LONGINT);
```

```python
def vs.NotifyPullDownClicked(nDialogID, nComponentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |

## Examples
```pascal
	BEGIN
boo := InsertPropClassOrLayerItem(dialog, 2*cnt+kUseDefaultClassButton, ObjectClassString, '');
 	NotifyPullDownClicked(dialog,2*cnt+kUseDefaultClassButton);
 	IF (tempS <> '') & (RecInfo[cnt].DefaultStrngClass <> '')THEN
 		BEGIN
 		IF GetObject(Concat(tempS,'-',RecInfo[cnt].DefaultStrngClass)) = NIL THEN {Class Already Exists}
 			boo := InsertPropClassOrLayerItem(dialog, 2*cnt+kUseDefaultClassButton, Concat(tempS,'-',RecInfo[cnt].DefaultStrngClass), '');
```
```python
import vs

# Sends an item hit notification when the pull down menu is clicked, allowing
# developers to dynamically populate the menu.
nDialogID = 1
nComponentID = 2

vs.NotifyPullDownClicked(nDialogID, nComponentID)
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
