# EnableLBExternalSort

## Description
Enables/disables external sorting.

```pascal
PROCEDURE EnableLBExternalSort(
				dialogID    : LONGINT;
				componentID : LONGINT;
				enable      : BOOLEAN);
```

```python
def vs.EnableLBExternalSort(dialogID, componentID, enable):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|enable|BOOLEAN|specifies whether to enable or disable external sorting|

## Examples
```pascal
{Key List}
boo:=EnableLBSingleLineSelection(dialogIDSetup, kBrowserKeyList, FALSE);
EnableLBSorting(dialogIDSetup, kBrowserKeyList, FALSE);
EnableLBExternalSort(dialogIDSetup, kBrowserKeyList, TRUE);
SetLBSortColumn(dialogIDSetup, kBrowserKeyList, 0, FALSE);
EnableLBColumnLines(dialogIDSetup, kBrowserKeyList, TRUE);
```
```python
import vs

# Enables/disables external sorting.
dialogID = 1
componentID = 2
enable = True

vs.EnableLBExternalSort(dialogID, componentID, enable)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
