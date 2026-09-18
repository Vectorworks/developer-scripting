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
WHILE h <> NIL DO BEGIN
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

```pascal
BEGIN
	BSB := AnnotateThings(FInGroup(itemHandle));
END;

BEGIN
CASE GetType(GetParent(parmHand)) OF
	11: ForEachObjectInList(Reset_Selection, 2, 0, FInGroup(GetParent(parmHand)));
	16: ForEachObjectInList(Reset_Selection, 2, 0, FInSymDef(GetParent(parmHand)));
	END;

BEGIN
		slab_h := fingroup(slab_h);
		WHILE (slab_h <> NIL) DO
		BEGIN
			IF gettype(slab_h) = 38 THEN
			BEGIN
```
```python
import vs

# Function FInGroup returns a handle to the first component object of the
# referenced group.
ObjectHd = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.FInGroup(ObjectHd)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
