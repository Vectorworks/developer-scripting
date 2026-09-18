# CreateLineWeightPopup

## Description
Create a line weight popup dialog control to display list of line weights available in current document.

```pascal
PROCEDURE CreateLineWeightPopup(
				dialogID : LONGINT;
				itemID   : LONGINT);
```

```python
def vs.CreateLineWeightPopup(dialogID, itemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |

## Examples
```pascal
CreatePulldownMenu        (dialog1, kPopup30,        20);
CreateStaticText		  (dialog1, kGridMarkerLLText,		GetStr(kGridMarkerLLText),		-1 );
   CreateEditReal			  (dialog1, kGridMarkerLLEditReal,	3, gGridMarkerLLength,	20 );
   CreateStaticText		  (dialog1, kGridMarkerLWText,		GetStr(kGridMarkerLWText),		-1 );
   CreateLineWeightPopup	  (dialog1, kGridMarkerLWPopup );
   CreateCheckBox			  (dialog1, kShowGridLineCheckBox,	GetStr(kShowGridLineCheckBox) );
   CreateStaticText		  (dialog1, kCountersignatureText,	GetStr(kCountersignatureText),	-1 );
   CreatePullDownMenu		  (dialog1, kCountersignaturePopup, 								20 );

CreateColorPopup(dialogID, 25, kColorWidth);			{pen color}
CreateLineWeightPopup(dialogID, 26);				{line weight}
CreateLineStylePopup(dialogID, 27);					{line style}
CreatePatternPopup(dialogID, 28);					{fill pattern}
CreateColorPopup(dialogID, 29, kForeBackColorWidth);		{fill fore color}
CreateColorPopup(dialogID, 30, kForeBackColorWidth);		{fill back color}

CreateStaticText( JoistAttributesDialogID, kLineWeightST, GetPluginString(3244), -1 );  {Lineweight:}
CreateLineWeightPopup( JoistAttributesDialogID, kLineWeightPDM );
CreateTabPane( JoistAttributesDialogID, kGraphTab, kGraphGroup);
```
```python
import vs

# Create a line weight popup dialog control to display list of line weights
# available in current document.
dialogID = 1
itemID = 2

vs.CreateLineWeightPopup(dialogID, itemID)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
