# Selected

## Description
Function Selected returns the selection status of the referenced object.

```pascal
FUNCTION Selected(h : HANDLE): BOOLEAN;
```

```python
def vs.Selected(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
```pascal
IF (GetType (h) = 6) AND (Selected (h)) THEN
BEGIN
	isArc := TRUE;
	objH := h;
END

BEGIN
	IF  ( ( bOnlySelected & Selected( textH )) | ( NOT bOnlySelected ) ) &
		( ObjLayerAndClassCheck( textH, SuportedLayers, SuportedClasses ) ) &
		( KeyNoteCheck( textH ) ) THEN BEGIN
		{save the handle of the text block object}
		tBlCnt := tBlCnt + 1;
		arrTBlocksH[ tBlCnt ] := textH;
		arrTBlocksUsed[ tBlCnt ] := FALSE;
	END;

BEGIN
	IF ((GetType (h) = 3) OR (GetType (h) = 5)) AND (Selected (h)) THEN
	BEGIN
		polyH := h;
		isPolyOrRect := TRUE;
	END
```
```python
import vs

# Function Selected returns the selection status of the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.Selected(h)
if ok:
    vs.Message('Selected succeeded')
else:
    vs.Message('Selected failed')
```

## Version
Availability: from All Versions

## Category
* [Selection](../Categories/Selection.md)
