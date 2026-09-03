# GetCablePartsCnt

## Description
Get the count of cable parts in the cable or cable section. If SectionIndex is set to 0 it will be ignored.

```pascal
FUNCTION GetCablePartsCnt(
				hObj         : HANDLE;
				SectionIndex : INTEGER) : INTEGER;
```

```python

def vs.GetCablePartsCnt(hObj, SectionIndex):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE||
|SectionIndex|INTEGER||

## Examples
```pascal
resultN := GetCablePartsCnt(hObj, 1);
```
```python
import vs

# Get the count of cable parts in the cable or cable section.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer
SectionIndex = 1

resultN = vs.GetCablePartsCnt(hObj, SectionIndex)
vs.Message('GetCablePartsCnt returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2025.4

## Category
* [Objects - Cables](../Categories/Objects%20-%20Cables.md)
