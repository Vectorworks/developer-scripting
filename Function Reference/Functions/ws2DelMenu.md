# ws2DelMenu

## Description
Workspace advanced APIs. Delete the menu at the specified menu path. See 'ws2GetMenusCnt'.

```pascal
FUNCTION ws2DelMenu(menuPath : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.ws2DelMenu(menuPath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultOK := ws2DelMenu(menuPath);
```
```python
import vs

# Workspace advanced APIs.
menuPath = 'C:/Temp'

ok = vs.ws2DelMenu(menuPath)
if ok:
    vs.Message('ws2DelMenu succeeded')
else:
    vs.Message('ws2DelMenu failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
