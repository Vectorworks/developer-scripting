# ws2AddMenuGroup

## Description
Workspace advanced APIs. Adds a new menu group (container) by universal name before the specified index (-1 for the end) inside the provided menu path. See 'ws2GetMenusCnt'.

```pascal
FUNCTION ws2AddMenuGroup(
				menuPath       : DYNARRAY[] of CHAR;
				newUnivName    : DYNARRAY[] of CHAR;
				newDisplayName : DYNARRAY[] of CHAR;
				beforeIndex    : INTEGER): BOOLEAN;
```

```python
def vs.ws2AddMenuGroup(menuPath, newUnivName, newDisplayName, beforeIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|DYNARRAY[] of CHAR|   |
|newUnivName|DYNARRAY[] of CHAR|   |
|newDisplayName|DYNARRAY[] of CHAR|   |
|beforeIndex|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
