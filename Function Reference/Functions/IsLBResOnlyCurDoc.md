# IsLBResOnlyCurDoc

## Description
Returns whether the specified list browser item is set, or not, to only use the current document when using/displaying resources.

```pascal
FUNCTION IsLBResOnlyCurDoc(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER): BOOLEAN;
```

```python
def vs.IsLBResOnlyCurDoc(dialogID, componentID, itemIndex, subItemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the item index|
|subItemIndex|INTEGER|the column index|

## Examples
```pascal
resultOK := IsLBResOnlyCurDoc(1, 2, 3, 10);
```
```python
import vs

# Returns whether the specified list browser item is set, or not, to only use
# the current document when using/displaying resources.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1

ok = vs.IsLBResOnlyCurDoc(dialogID, componentID, itemIndex, subItemIndex)
if ok:
    vs.Message('IsLBResOnlyCurDoc succeeded')
else:
    vs.Message('IsLBResOnlyCurDoc failed')
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
