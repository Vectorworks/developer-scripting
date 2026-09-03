# SetSelect

## Description
Procedure SetSelect selects the referenced object.

```pascal
PROCEDURE SetSelect(h : HANDLE);
```

```python
def vs.SetSelect(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
To select an object in a Wall you must select both the object and the Wall.

## Examples
```pascal
BEGIN
	SetSelect(RedList[TmpIndex]);
	{DoMenuTextByName(kDoMenuUnlock, 0); }{Unlock The redline object}
	UnLckObjs;{Unlock The redline object}
	SetRL(RedList[TmpIndex], TheRLStatus); {Pick Up/ Restore The Redline}
	IF GetType(RedList[TmpIndex]) = 11 THEN {Only re-lock the redline if it is an old style redline}

BEGIN
	wallH1 := wallH [i];
	SetSelect (wallH1);
	IF (NOT useStyle) & (NOT useHeight) THEN
		OK := SetWallOverallHeights(wallH1,0,0,'',0,0,0,'',deltaZ);

	END;
	i := i + 1;
END;
IF (traversalOpts = 2) & (hasParent) THEN AlrtDialog(GetPlugInString(7001));
if WhatToDo = 'add' then for i := 1 to handle_cnt do SetSelect(handles[i]) ELSE
if WhatToDo = 'rem' then for i := 1 to handle_cnt do SetDSelect(handles[i]) ELSE
if WhatToDo = 'new' then BEGIN
	for i := 1 to select_cnt DO SetDSelect(selects[i]);
	for i := 1 to handle_cnt DO SetSelect(handles[i]);
	list_cnt := 0;
	for i := 1 to handle_cnt DO BEGIN
		tmpStr := GetClass(handles[i]);
```
```python
import vs

# Procedure SetSelect selects the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.SetSelect(h)
```
See also in tutorials: [10. Iterate the Drawing and Report a Summary](ai%20examples/10_IterateAndReport.md)

## Version
Availability: from All Versions

## Category
* [Selection](../Categories/Selection.md)
