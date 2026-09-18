# GetNumLBItems

## Description
Gets the number of items in the specified list browser control.

```pascal
FUNCTION GetNumLBItems(
				dialogID    : LONGINT;
				componentID : LONGINT): INTEGER;
```

```python
def vs.GetNumLBItems(dialogID, componentID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|

## Examples
```pascal
BEGIN
	rowID := -1; {the standard value for nothing selected}
	for cnt := 0 to GetNumLBItems(dialogID, controlID) - 1 do BEGIN
		if IsLBItemSelected(dialogID, controlID, cnt) then BEGIN
			rowID := cnt;
			boo := GetLBItemInfo(dialogID, controlID, cnt, columnID, textStr, cnt);
			cnt := GetNumLBItems(dialogID, controlID);
		END;

	BEGIN
		str1 		:= gRefClassNames [i];
		str2 		:= gActClassNames [i];
		iLib 		:= GetNumLBItems(dialogID, itemID);
		tempResInt 	:= InsertLBItem(dialogID, itemID, iLib, str1);
		tempResBool	:= SetLBItemInfo(dialogID, itemID, iLib, 1, str2, 0);
	END;	{of i := 1 TO gNumClasses DO}
END;	{of gSetUpChoiceI = 1}

	if NOT tmpBool_7 then EnableItem(dialogID, 14, FALSE);
	IF NOT (tmpBool_6 | tmpBool_7) THEN item := -1;
END;
1:	BEGIN
	For cnt := 1 to GetNumLBItems(dialogID, 5) do BEGIN
		BSB := GetLBItemInfo(dialogID, 5, cnt-1, 0, str, temp_i);
		BSB := GetLBItemInfo(dialogID, 5, cnt-1, 1, layers[cnt].name, temp_i);
		layers[cnt].sel := Str2Boo(str);
	END;
```
```python
import vs

# Gets the number of items in the specified list browser control.
dialogID = 1
componentID = 2

count = vs.GetNumLBItems(dialogID, componentID)
vs.Message('GetNumLBItems returned: ' + str(count))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
