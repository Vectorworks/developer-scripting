# RemoveLBColumnDataItem

## Description
Removes the specified column data item.

```pascal
FUNCTION RemoveLBColumnDataItem(
				dialogID            : LONGINT;
				componentID         : LONGINT;
				columnIndex         : INTEGER;
				columnDataItemIndex : INTEGER): BOOLEAN;
```

```python
def vs.RemoveLBColumnDataItem(dialogID, componentID, columnIndex, columnDataItemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|columnDataItemIndex|INTEGER|the column data item to remove|

## Examples
```pascal
For cnt := 1 to gNumLabelLegends DO
	IF LegendSymbol[cnt,1].LegendSymName = gLegendName THEN LegendSymbol[cnt,1].LegendSymName := '';
boo := DeleteLBItem(ChooseLegend, kChooseLB,rowID);
boo := FindLBColumnDataItem(ChooseLegend, kChooseLB, kColLegendName, gLegendName ,rowID);
boo := RemoveLBColumnDataItem(ChooseLegend, kChooseLB, kColLegendName, rowID);
LB_GetSelChoice(ChooseLegend, kChooseLB, kColLegendName, rowID,textStr);
IF rowID = -1 THEN
	BEGIN
	EnableItem(ChooseLegend, kRemove,FALSE);
```
```python
import vs

# Removes the specified column data item.
dialogID = 1
componentID = 2
columnIndex = 1
columnDataItemIndex = 1

ok = vs.RemoveLBColumnDataItem(dialogID, componentID, columnIndex, columnDataItemIndex)
if ok:
    vs.Message('RemoveLBColumnDataItem succeeded')
else:
    vs.Message('RemoveLBColumnDataItem failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
