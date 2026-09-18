# CreateLineStylePopup

## Description
Create a dialog control that displays the line style choices available in the active document.

```pascal
PROCEDURE CreateLineStylePopup(
				dialogID : LONGINT;
				itemID   : LONGINT);
```

```python
def vs.CreateLineStylePopup(dialogID, itemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |

## Remarks
Create a dialog control that displays the line style choices available in the active document.

## Examples
```pascal
CreateLineStylePopup( dialogID, MeasureLineStylePop_ID );
SetRightItem( dialogID, MeasureLineStyleStaTex_ID, MeasureLineStylePop_ID, 0, 0 );

CreateColorPopup(dialogID, 25, kColorWidth);			{pen color}
CreateLineWeightPopup(dialogID, 26);				{line weight}
CreateLineStylePopup(dialogID, 27);					{line style}
CreatePatternPopup(dialogID, 28);					{fill pattern}
CreateColorPopup(dialogID, 29, kForeBackColorWidth);		{fill fore color}
CreateColorPopup(dialogID, 30, kForeBackColorWidth);		{fill back color}
```
```python
import vs

# Create a dialog control that displays the line style choices available in
# the active document.
dialogID = 1
itemID = 2

vs.CreateLineStylePopup(dialogID, itemID)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
