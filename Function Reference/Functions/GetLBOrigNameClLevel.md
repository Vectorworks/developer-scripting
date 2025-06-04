# GetLBOrigNameClLevel

## Description
This function returns the close levels for an original name in the list browser. If the item for the name is displayed, then all the closeLevels will be false.

```pascal
PROCEDURE GetLBOrigNameClLevel(
				dialogID         : LONGINT;
				componentID      : LONGINT;
				originalName     : STRING;
				VAR level1Closed : BOOLEAN;
				VAR level2Closed : BOOLEAN;
				VAR level3Closed : BOOLEAN);
```

```python
def vs.GetLBOrigNameClLevel(dialogID, componentID, originalName):
    return (level1Closed, level2Closed, level3Closed)
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
