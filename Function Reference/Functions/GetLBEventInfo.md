# GetLBEventInfo

## Description
Retrieves the last event information for the specified list browser.

```pascal
FUNCTION GetLBEventInfo(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				VAR eventType  : INTEGER;
				VAR rowIndex   : INTEGER;
				VAR columIndex : INTEGER): BOOLEAN;
```

```python
def vs.GetLBEventInfo(dialogID, componentID):
    return (BOOLEAN, eventType, rowIndex, columIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|eventType|INTEGER|   |
|rowIndex|INTEGER|the row index where the click occurred.|
|columIndex|INTEGER|the column index where the click occurred.|

## Remarks
'''eventType'''
<lineList ident=1>
<line>
kMessageDataChangeClick	             = -2;
</line>
<line>
kMessageDataChangeAllClick           = -3;
</line>
<line>
kMessageSelectionChangeClick         = -4;
</line>
<line>
kMessageDoubleClick                  = -5;
</line>
<line>
kMessageDeleteKeyPressed             = -6;
</line>
<line>
kMessageUpKeyPressed                 = -7;
</line>
<line>
kMessageDownKeyPressed               = -8;
</line>
<line>
kMessageAlphaNumericKeyPressed       = -9;
</line>
<line>
kMessageSortOccurred                 = -10;
</line>
<line>
kMessageEnterKeyPressed              = -12;
</line>
<line>
kMessageDataChangeRecursiveClick     = -13;
</line>
<line>
kMessageDoubleAllClick               = -14;
</line>
<line>
kMessageDoubleRecursiveClick         = -15;
</line>
</lineList>

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
