# OLDGetHangPointsCnt

## Description
Get hang points cout of the specified load for the parametric object

```pascal
FUNCTION OLDGetHangPointsCnt(
				handle    : HANDLE;
				loadIndex : INTEGER): LONGINT;
```

```python
def vs.OLDGetHangPointsCnt(handle, loadIndex):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|loadIndex|INTEGER|   |

## Examples
```pascal
BEGIN
	lenght		:= 0;
    versCount	:= OLDGetHangPointsCnt( loadObj, loadIndex );
	IF versCount > 1 THEN
	BEGIN
		OLDGetHangPointAt( loadObj, loadIndex, 1, prevPt, prevHasLoad );
		FOR index := 2 TO versCount DO
```
```python
import vs

# Get hang points cout of the specified load for the parametric object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
loadIndex = 1

resultN = vs.OLDGetHangPointsCnt(handle, loadIndex)
vs.Message('OLDGetHangPointsCnt returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
