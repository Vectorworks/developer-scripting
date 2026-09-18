# SetToolByIndex

## Description
Similar to SetTool. Takes the internal ID of a tool.

```pascal
FUNCTION SetToolByIndex(toolIndex : INTEGER): BOOLEAN;
```

```python
def vs.SetToolByIndex(toolIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolIndex|INTEGER|   |

## Examples
```pascal
resultOK := SetToolByIndex(1);
```
```python
import vs

# Similar to SetTool.
toolIndex = 1

ok = vs.SetToolByIndex(toolIndex)
if ok:
    vs.Message('SetToolByIndex succeeded')
else:
    vs.Message('SetToolByIndex failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
