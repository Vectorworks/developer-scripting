# IsLBSortingEnabled

## Description
Determines if sorting is enabled or disabled.

```pascal
FUNCTION IsLBSortingEnabled(
				dialogID    : LONGINT;
				componentID : LONGINT): BOOLEAN;
```

```python
def vs.IsLBSortingEnabled(dialogID, componentID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|

## Examples
```pascal
resultOK := IsLBSortingEnabled(1, 2);
```
```python
import vs

# Determines if sorting is enabled or disabled.
dialogID = 1
componentID = 2

ok = vs.IsLBSortingEnabled(dialogID, componentID)
if ok:
    vs.Message('IsLBSortingEnabled succeeded')
else:
    vs.Message('IsLBSortingEnabled failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
