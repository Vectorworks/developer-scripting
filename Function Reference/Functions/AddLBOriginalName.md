# AddLBOriginalName

## Description
This function is called when hierarchical display is on and a new item is added to the list browser.

```pascal
PROCEDURE AddLBOriginalName(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				originalName : STRING);
```

```python
def vs.AddLBOriginalName(dialogID, componentID, originalName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog.|
|componentID|LONGINT|The id of the list browser.|
|originalName|STRING|The original name of the new item being added to the list browser.|

## Examples
```pascal
AddLBOriginalName(1, 2, 'Example');
```
```python
import vs

# This function is called when hierarchical display is on and a new item is
# added to the list browser.
dialogID = 1
componentID = 2
originalName = 'Example'

vs.AddLBOriginalName(dialogID, componentID, originalName)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
