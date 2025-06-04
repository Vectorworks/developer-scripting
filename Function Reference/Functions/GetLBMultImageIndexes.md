# GetLBMultImageIndexes

## Description
Gets the index of the images within the list browser multi image display.

```pascal
FUNCTION GetLBMultImageIndexes(
				dialogID        : LONGINT;
				componentID     : LONGINT;
				itemIndex       : INTEGER;
				subItemIndex    : INTEGER;
				VAR imageIndex0 : INTEGER;
				VAR imageIndex1 : INTEGER;
				VAR imageIndex2 : INTEGER): BOOLEAN;
```

```python
def vs.GetLBMultImageIndexes(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, imageIndex0, imageIndex1, imageIndex2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|imageIndex0|INTEGER|the 'ics8' resource index of the first image|
|imageIndex1|INTEGER|the 'ics8' resource index of the second image|
|imageIndex2|INTEGER|the 'ics8' resource index of the third image|

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
