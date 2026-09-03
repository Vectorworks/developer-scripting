# Hide

## Description
Hides any visible or grayed objects matching the specified search criteria.

```pascal
PROCEDURE Hide(c : CRITERIA);
```

```python
def vs.Hide(c):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Remarks
Makes objects with the specified search criteria invisible if they are not already

## Examples
#### VectorScript ####
```pascal
Hide((C='Proposed Phase 2 Construction'));
```
#### Python ####
```python

```

```pascal
		SetClassOptions(5);
		for i := 1 to ClassNum DO ShowClass(ClassList(i));
	END;
	str := Concat('(NOT', SQL, ')');
	Hide(str);
	Show('((SEL))');
	if (WhatToDo = 'new') | (WhatToDo = 'add') then FOR i := 1 to handle_cnt DO ReallyShowEm(handles[i]);
	DoMenuTextByName(GetLocStr(11050, 13), 0); {'Fit To Objects'}
END;
```
```python
vs.Hide(c)
```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
