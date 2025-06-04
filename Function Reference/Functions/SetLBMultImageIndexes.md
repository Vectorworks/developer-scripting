# SetLBMultImageIndexes

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See [[VS:SetLBImageIndexes|SetLBImageIndexes]] for a replacement.

Sets the index of the images within the list browser multi image display.

```pascal
FUNCTION SetLBMultImageIndexes(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				imageIndex0  : INTEGER;
				imageIndex1  : INTEGER;
				imageIndex2  : INTEGER): BOOLEAN;
```

```python
def vs.SetLBMultImageIndexes(dialogID, componentID, itemIndex, subItemIndex, imageIndex0, imageIndex1, imageIndex2):
    return BOOLEAN
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
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
