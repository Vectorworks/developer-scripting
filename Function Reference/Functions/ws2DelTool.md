# ws2DelTool

## Description
Workspace advanced APIs. Delete the tool, tool set, or tool palette at the specified menu path. See 'ws2GetMenusCnt'.

```pascal
FUNCTION ws2DelTool(toolPath : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.ws2DelTool(toolPath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolPath|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultOK := ws2DelTool(toolPath);
```
```python
import vs

# Workspace advanced APIs.
toolPath = 'C:/Temp'

ok = vs.ws2DelTool(toolPath)
if ok:
    vs.Message('ws2DelTool succeeded')
else:
    vs.Message('ws2DelTool failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
