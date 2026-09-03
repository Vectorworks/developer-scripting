# SetLBMultImageIndexes

## Description
_[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)_. See [SetLBImageIndexes](SetLBImageIndexes.md) for a replacement.

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

## Examples
```pascal
resultOK := SetLBMultImageIndexes(1, 2, 3, 10, 5, 1, 2);
```
```python
import vs

# _Vectorworks 2012 Deprecated Functions_.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
imageIndex0 = 1
imageIndex1 = 1
imageIndex2 = 1

ok = vs.SetLBMultImageIndexes(dialogID, componentID, itemIndex, subItemIndex, imageIndex0, imageIndex1, imageIndex2)
if ok:
    vs.Message('SetLBMultImageIndexes succeeded')
else:
    vs.Message('SetLBMultImageIndexes failed')
```

## Version
Availability: from VectorWorks12.0
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
