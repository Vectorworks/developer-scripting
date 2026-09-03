# GetLBItemPatternIndex

## Description
Gets the specified list browser item's pattern index.

```pascal
FUNCTION GetLBItemPatternIndex(
				dialogID         : LONGINT;
				componentID      : LONGINT;
				itemIndex        : INTEGER;
				the column index : INTEGER;
				VAR outPatIndex  : INTEGER): BOOLEAN;
```

```python
def vs.GetLBItemPatternIndex(dialogID, componentID, itemIndex, the column index):
    return (BOOLEAN, outPatIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|the column index|INTEGER|the column index|
|outPatIndex|INTEGER|Output parameter. Returns the pattern index of this item. Value from [1..71] see [Sciprt Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).|

## Examples
```pascal
resultOK := GetLBItemPatternIndex(1, 2, 3, 10, 5);
```
```python
import vs

# Gets the specified list browser item's pattern index.
dialogID = 1
componentID = 2
itemIndex = 1
the column index = 1

ok, outPatIndex = vs.GetLBItemPatternIndex(dialogID, componentID, itemIndex, the column index)
vs.Message('GetLBItemPatternIndex returned: ' + str((ok, outPatIndex)))
```

## See Also
[SetLBItemPatternIndex](SetLBItemPatternIndex.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
