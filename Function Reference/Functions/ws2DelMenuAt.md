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

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
