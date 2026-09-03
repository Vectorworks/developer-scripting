# GetComponentTextWidth

## Description
Retrieves the static text's width in Layout Manager Units.

```pascal
FUNCTION GetComponentTextWidth(
				nDialogID           : LONGINT;
				nComponentID        : LONGINT;
				VAR nWidthInLMUnits : INTEGER): BOOLEAN;
```

```python
def vs.GetComponentTextWidth(nDialogID, nComponentID):
    return (BOOLEAN, nWidthInLMUnits)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nWidthInLMUnits|INTEGER|   |

## Examples
```pascal
resultOK := GetComponentTextWidth(1, 2, 3);
```
```python
import vs

# Retrieves the static text's width in Layout Manager Units.
nDialogID = 1
nComponentID = 2

ok, nWidthInLMUnits = vs.GetComponentTextWidth(nDialogID, nComponentID)
vs.Message('GetComponentTextWidth returned: ' + str((ok, nWidthInLMUnits)))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
