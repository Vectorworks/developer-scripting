# IsLBReadOnly

## Description
Determines the list browser's read-only state.

```pascal
FUNCTION IsLBReadOnly(
				dialogID    : LONGINT;
				componentID : LONGINT): BOOLEAN;
```

```python
def vs.IsLBReadOnly(dialogID, componentID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |

## Examples
```pascal
resultOK := IsLBReadOnly(1, 2);
```
```python
import vs

# Determines the list browser's read-only state.
dialogID = 1
componentID = 2

ok = vs.IsLBReadOnly(dialogID, componentID)
if ok:
    vs.Message('IsLBReadOnly succeeded')
else:
    vs.Message('IsLBReadOnly failed')
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
