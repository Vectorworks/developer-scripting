# EnableLBRadioColumnLines

## Description
Enables/disables radio item &quot;column&quot; lines.

```pascal
PROCEDURE EnableLBRadioColumnLines(
				dialogID               : LONGINT;
				componentID            : LONGINT;
				columnIndex            : INTEGER;
				enableRadioColumnLines : BOOLEAN);
```

```python
def vs.EnableLBRadioColumnLines(dialogID, componentID, columnIndex, enableRadioColumnLines):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|enableRadioColumnLines|BOOLEAN|specifies if radio item &quot;column&quot; lines should be drawn|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
