# SetMaximumUndoEvents

## Description
Procedure SetMaximumUndoEvents sets the maximum number of undo events that can be stored in the undo table. Parameter events specifies the number of undos. Setting this value to zero effectively turns off undo.

```pascal
PROCEDURE SetMaximumUndoEvents(events : INTEGER);
```

```python
def vs.SetMaximumUndoEvents(events):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|events|INTEGER|Number of undo events to store.|

## Remarks
Sets the maximum number of undo events that can be stored in the undo table. Setting this to zero effectively turns off undo.

## Version
Availability: from VectorWorks8.0

## Category
* [Utility](../Categories/Utility.md)
