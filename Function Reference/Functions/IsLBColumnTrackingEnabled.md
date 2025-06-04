# IsLBColumnTrackingEnabled

## Description
Determines if column tracking is enabled for the specified column.

```pascal
FUNCTION IsLBColumnTrackingEnabled(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): BOOLEAN;
```

```python
def vs.IsLBColumnTrackingEnabled(dialogID, componentID, columnIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
