# RefreshLB

## Description
Refreshes the contents of the specified list browser.

```pascal
FUNCTION RefreshLB(
				dialogID    : LONGINT;
				componentID : LONGINT): BOOLEAN;
```

```python
def vs.RefreshLB(dialogID, componentID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|

## Examples
```pascal
tempResBool := RefreshLB(dialogID, itemID);

			IF cnt-1 <> rowIndex THEN LB_SetCell(ChooseLegend, kChooseLB, cnt-1, kColActive, 'False');
			END;
		END;
	END;
boo := RefreshLB(ChooseLegend, kChooseLB);
END;

	BSB := RefreshLB(dialog, kArrayStackLB);
END;
```
```python
import vs

# Refreshes the contents of the specified list browser.
dialogID = 1
componentID = 2

ok = vs.RefreshLB(dialogID, componentID)
if ok:
    vs.Message('RefreshLB succeeded')
else:
    vs.Message('RefreshLB failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
