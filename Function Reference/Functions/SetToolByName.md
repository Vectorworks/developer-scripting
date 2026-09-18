# SetToolByName

## Description
Similar to SetTool, but takes name rather than ID. Supports plug-in tools (but not yet internal tools).

```pascal
FUNCTION SetToolByName(toolName : STRING): BOOLEAN;
```

```python
def vs.SetToolByName(toolName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolName|STRING|   |

## Examples
```pascal
resultOK := SetToolByName('Example');
```
```python
import vs

# Similar to SetTool, but takes name rather than ID.
toolName = 'Example'

ok = vs.SetToolByName(toolName)
if ok:
    vs.Message('SetToolByName succeeded')
else:
    vs.Message('SetToolByName failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
