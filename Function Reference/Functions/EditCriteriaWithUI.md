# EditCriteriaWithUI

## Description
Edit a criteria string with Edit Criteria Dialog.

```pascal
FUNCTION EditCriteriaWithUI(VAR criteria : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.EditCriteriaWithUI(criteria):
    return (INTEGER, criteria)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|criteria|DYNARRAY[] of CHAR|Pass in a criteria to be edited, and output the modified criteria if the function result is TRUE.|

## Examples
```pascal
END;
kButtonCriteria  : BEGIN
	GetItemText(dialogIDFilters, kBrowserCustom, tempStr);
	critStr:=Concat(tempStr);
	CASE EditCriteriaWithUI(critStr) OF
		0: {Fail} BEGIN
			SysBeep;
			EnableItem(dialogIDFilters, kOK, FALSE);
			EnableItem(dialogIDFilters, kButtonCriteria, FALSE);
			SelectEditText(dialogIDFilters, kBrowserCustom);
		END;
```
```python
import vs

# Edit a criteria string with Edit Criteria Dialog.
criteria = "(SEL=TRUE)"  # selection criteria - all selected objects

resultN, criteria = vs.EditCriteriaWithUI(criteria)
vs.Message('EditCriteriaWithUI returned: ' + str((resultN, criteria)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
