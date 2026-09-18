# AreLBRadioColumnLinesEnabled

## Description
Determines if &quot;column&quot; lines are drawn between radio control items.

```pascal
FUNCTION AreLBRadioColumnLinesEnabled(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): BOOLEAN;
```

```python
def vs.AreLBRadioColumnLinesEnabled(dialogID, componentID, columnIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|

## Examples
```pascal
resultOK := AreLBRadioColumnLinesEnabled(1, 2, 3);
```
```python
import vs

# Determines if &quot;column&quot; lines are drawn between radio control items.
dialogID = 1
componentID = 2
columnIndex = 1

ok = vs.AreLBRadioColumnLinesEnabled(dialogID, componentID, columnIndex)
if ok:
    vs.Message('AreLBRadioColumnLinesEnabled succeeded')
else:
    vs.Message('AreLBRadioColumnLinesEnabled failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
