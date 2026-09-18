# DT_UpdateTaggedTags

## Description
Returns TRUE if updating is successful.

```pascal
FUNCTION DT_UpdateTaggedTags(h : HANDLE): BOOLEAN;
```

```python
def vs.DT_UpdateTaggedTags(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
resultOK := DT_UpdateTaggedTags(h);
```
```python
import vs

# Returns TRUE if updating is successful.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.DT_UpdateTaggedTags(h)
if ok:
    vs.Message('DT_UpdateTaggedTags succeeded')
else:
    vs.Message('DT_UpdateTaggedTags failed')
```

## Version
Availability: from Vectorworks 2019

## Category
* [Data Tag Interface Library](../Categories/Data%20Tag%20Interface%20Library.md)
