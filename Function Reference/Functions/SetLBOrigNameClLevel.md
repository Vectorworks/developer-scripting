# SetLBOrigNameClLevel

## Description
This function sets the closed levels for an original item in the list browser. The item will be hidden and the proper container closed.

```pascal
PROCEDURE SetLBOrigNameClLevel(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				originalName : STRING;
				level1Closed : BOOLEAN;
				level2Closed : BOOLEAN;
				level3Closed : BOOLEAN);
```

```python
def vs.SetLBOrigNameClLevel(dialogID, componentID, originalName, level1Closed, level2Closed, level3Closed):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog.|
|componentID|LONGINT|The id of the list browser.|
|originalName|STRING|The original name of the item.|
|level1Closed|BOOLEAN|Whether the item's level 1 container is closed.|
|level2Closed|BOOLEAN|Whether the item's level 2 container is closed.|
|level3Closed|BOOLEAN|Whether the item's level 3 container is closed.|

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
