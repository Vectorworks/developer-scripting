# ws2DelMenuAt

## Description
Workspace advanced APIs. Delete the menu at the specified index and menu path. See 'ws2GetMenusCnt'.

```pascal
FUNCTION ws2DelMenuAt(
				menuPath : DYNARRAY[] of CHAR;
				index    : INTEGER): BOOLEAN;
```

```python
def vs.ws2DelMenuAt(menuPath, index):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|DYNARRAY[] of CHAR|   |
|index|INTEGER|   |

## Examples
```pascal
resultOK := ws2DelMenuAt(menuPath, 1);
```
```python
import vs

# Workspace advanced APIs.
menuPath = 'C:/Temp'
index = 1

ok = vs.ws2DelMenuAt(menuPath, index)
if ok:
    vs.Message('ws2DelMenuAt succeeded')
else:
    vs.Message('ws2DelMenuAt failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
