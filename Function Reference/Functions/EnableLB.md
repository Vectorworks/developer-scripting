# EnableLB

## Description
Enables or disables the specified list browser.

```pascal
FUNCTION EnableLB(
				dialogID    : LONGINT;
				componentID : LONGINT;
				enable      : BOOLEAN): BOOLEAN;
```

```python
def vs.EnableLB(dialogID, componentID, enable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|enable|BOOLEAN|determines if the list browser should be enabled or disabled.|

## Examples
```pascal
resultOK := EnableLB(1, 2, TRUE);
```
```python
import vs

# Enables or disables the specified list browser.
dialogID = 1
componentID = 2
enable = True

ok = vs.EnableLB(dialogID, componentID, enable)
if ok:
    vs.Message('EnableLB succeeded')
else:
    vs.Message('EnableLB failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
