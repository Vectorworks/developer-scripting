# GetNumWallPeaks

## Description
Returns the number of peaks in the referenced wall.

```pascal
FUNCTION GetNumWallPeaks(h : HANDLE): INTEGER;
```

```python
def vs.GetNumWallPeaks(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to wall.|

## Remarks
return number of peaks in wall

## Examples
```pascal
{looking for those peaks between which we will be finding wall height}
i := 0;
bBottomPrep 	:= FALSE;
WHILE (i < GetNumWallPeaks(WallH)) AND (NOT bBottomPrep) DO BEGIN
	i := i + 1;
```
```python
import vs

# Returns the number of peaks in the referenced wall.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.GetNumWallPeaks(h)
vs.Message('GetNumWallPeaks returned: ' + str(count))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
