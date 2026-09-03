# EnableLBClickAllDataChange

## Description
Enables all radio and multi state column data items to be changed with a single click if the alt key or option key is pressed during the click.

```pascal
FUNCTION EnableLBClickAllDataChange(
				dialogID    : LONGINT;
				componentID : LONGINT;
				enable      : BOOLEAN): BOOLEAN;
```

```python
def vs.EnableLBClickAllDataChange(dialogID, componentID, enable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|enable|BOOLEAN|determines if all data items should be changed during the click if the appropriate modifier key is pressed.|

## Examples
```pascal
resultOK := EnableLBClickAllDataChange(1, 2, TRUE);
```
```python
import vs

# Enables all radio and multi state column data items to be changed with a
# single click if the alt key or option key is pressed during the click.
dialogID = 1
componentID = 2
enable = True

ok = vs.EnableLBClickAllDataChange(dialogID, componentID, enable)
if ok:
    vs.Message('EnableLBClickAllDataChange succeeded')
else:
    vs.Message('EnableLBClickAllDataChange failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
