# GetCableSectionsCnt

## Description
Get the count of cable sections in the cable.

```pascal
FUNCTION GetCableSectionsCnt(hObj : HANDLE) : INTEGER;
```

```python

def vs.GetCableSectionsCnt(hObj):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE||

## Examples
```pascal
resultN := GetCableSectionsCnt(hObj);
```
```python
import vs

# Get the count of cable sections in the cable.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetCableSectionsCnt(hObj)
vs.Message('GetCableSectionsCnt returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2025.4

## Category
* [Objects - Cables](../Categories/Objects%20-%20Cables.md)
