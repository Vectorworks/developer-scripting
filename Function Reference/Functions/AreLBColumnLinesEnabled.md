# AreLBColumnLinesEnabled

## Description
Determines if column lines are drawn.

```pascal
FUNCTION AreLBColumnLinesEnabled(
				dialogID    : LONGINT;
				componentID : LONGINT): BOOLEAN;
```

```python
def vs.AreLBColumnLinesEnabled(dialogID, componentID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|

## Examples
```pascal
resultOK := AreLBColumnLinesEnabled(1, 2);
```
```python
import vs

# Determines if column lines are drawn.
dialogID = 1
componentID = 2

ok = vs.AreLBColumnLinesEnabled(dialogID, componentID)
if ok:
    vs.Message('AreLBColumnLinesEnabled succeeded')
else:
    vs.Message('AreLBColumnLinesEnabled failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
