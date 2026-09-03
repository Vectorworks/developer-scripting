# EnableLBColumnLines

## Description
Enables/disables column lines.

```pascal
PROCEDURE EnableLBColumnLines(
				dialogID          : LONGINT;
				componentID       : LONGINT;
				enableColumnLines : BOOLEAN);
```

```python
def vs.EnableLBColumnLines(dialogID, componentID, enableColumnLines):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|enableColumnLines|BOOLEAN|specifies if column lines should be drawn|

## Examples
```pascal
		LB_SetCell(IDLabelDialog,kDataBox,i-1,0,Num2Str(0,i));
		LB_SetCell(IDLabelDialog,kDataBox,i-1,1,gDataArr[i,1]);
		LB_SetCell(IDLabelDialog,kDataBox,i-1,2,gDataArr[i,2]);
	END;
	EnableLBColumnLines(IDLabelDialog,kDataBox,TRUE);
	boo := SetLBSelection(IDLabelDialog,kDataBox,0,0,TRUE);
END;

EnableLBColumnLines(dlogID,5,TRUE);
SelectChoice(dlogID, 7,gViewIndex,TRUE);
END;

	EnableLBSorting(dlogID, itemID, FALSE);
	EnableLBColumnLines(dlogID, itemID, TRUE);
	tempRes := EnableLBSingleLineSelection(dlogID, itemID, TRUE);
END;
```
```python
import vs

# Enables/disables column lines.
dialogID = 1
componentID = 2
enableColumnLines = True

vs.EnableLBColumnLines(dialogID, componentID, enableColumnLines)
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
