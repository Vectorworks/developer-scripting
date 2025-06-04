# FInGroup

## Description
Function FInGroup returns a handle to the first component object of the referenced group.

```pascal
FUNCTION FInGroup(ObjectHd : HANDLE): HANDLE;
```

```python
def vs.FInGroup(ObjectHd):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ObjectHd|HANDLE|Handle to group object.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
h := FInGroup(FSActLayer);
WHILE h &lt;&gt; NIL DO BEGIN
SetClass(h, 'None');
h := NextObj(h);
END;
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	tmph = vs.FSActLayer()
	if tmph != 0:
		h = vs.FInGroup(tmph)
		if  h != 0:			
			vs.SetClass(h, 'None')
			h = vs.NextObj(h)
Example()
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
