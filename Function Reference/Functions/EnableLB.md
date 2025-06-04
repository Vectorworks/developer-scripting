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

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
