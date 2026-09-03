# CreatePatternPopup

## Description
Create a pattern popup dialog control that displays all fill patterns available in current document.

```pascal
PROCEDURE CreatePatternPopup(
				dialogID : LONGINT;
				itemID   : LONGINT);
```

```python
def vs.CreatePatternPopup(dialogID, itemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |

## Examples
```pascal
CreateGroupBox( dialogID, kFillPatternGroup, '', False );
CreateStaticText( dialogID, kstPattern, GetStr2(kstPattern), -1 );
CreatePatternPopup( dialogID, kPatternPopupID );
SetHelpText(dialogID, kPatternPopupID, GetHelpStr(2));

CreateColorPopup(dialogID, 25, kColorWidth);			{pen color}
CreateLineWeightPopup(dialogID, 26);				{line weight}
CreateLineStylePopup(dialogID, 27);					{line style}
CreatePatternPopup(dialogID, 28);					{fill pattern}
CreateColorPopup(dialogID, 29, kForeBackColorWidth);		{fill fore color}
CreateColorPopup(dialogID, 30, kForeBackColorWidth);		{fill back color}
```
```python
import vs

# Create a pattern popup dialog control that displays all fill patterns
# available in current document.
dialogID = 1
itemID = 2

vs.CreatePatternPopup(dialogID, itemID)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
