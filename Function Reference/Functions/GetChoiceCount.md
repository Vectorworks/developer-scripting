# GetChoiceCount

## Description
Gets the number of items in the component that contains the choices.

```pascal
PROCEDURE GetChoiceCount(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				VAR outCount : INTEGER);
```

```python
def vs.GetChoiceCount(dialogID, componentID):
    return outCount
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the component that contains the choices.|
|outCount|INTEGER|The number of items in the component.|

## Examples
```pascal
BEGIN
	gIsPopupField := TRUE;
	GetChoiceCount (dialogID, 14, existingCount);
	FOR i := 1 TO existingCount DO
		RemoveChoice (dialogID, 14, 0);
	FOR i := 1 TO gNumPopupValues DO
		AddChoice (dialogID, 14, popupValues [i], i - 1);

GetChoiceCount(dlogID, 22, itemCount);

GetChoiceText(dialogID, popupID, 1, strg);
ColorIndexToRGB(Str2Num(strg), r2, g2, b2);
diff := ColorDiff(r1, g1, b1, r2, g2, b2);
colorStr := strg;
GetChoiceCount(dialogID, popupID, itemCount);
```
```python
import vs

# Gets the number of items in the component that contains the choices.
dialogID = 1
componentID = 2

result = vs.GetChoiceCount(dialogID, componentID)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
