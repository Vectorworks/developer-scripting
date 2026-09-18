# SetDSelect

## Description
Procedure SetDSelect deselects the referenced object.

```pascal
PROCEDURE SetDSelect(h : HANDLE);
```

```python
def vs.SetDSelect(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
[IsolateLayer](examples/IsolateLayer.md)

```pascal
	SetRL(RedList[TmpIndex], TheRLStatus); {Pick Up/ Restore The Redline}
	IF GetType(RedList[TmpIndex]) = 11 THEN {Only re-lock the redline if it is an old style redline}
		{DoMenuTextByName(kDoMenuLock, 0);}{Re-Lock the redline object}
			LckObjs;{Re-Lock the redline object}
	SetDSelect(RedList[TmpIndex]); {Deselect the RedLine}
END;

BEGIN
	rectH := polyH;
	SetDSelect (rectH);
	polyH := ConvertToPolyline( HDuplicate( polyH, 0, 0 ) );
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

# Procedure SetDSelect deselects the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.SetDSelect(h)
```

## Version
Availability: from All Versions

## Category
* [Selection](../Categories/Selection.md)
