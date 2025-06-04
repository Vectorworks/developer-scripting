# ws2SetToolInfo

## Description
Workspace advanced APIs. Set the tool information at the specified index of the parent tool at the specified path. See 'ws2GetToolsCnt'.

```pascal
PROCEDURE ws2SetToolInfo(
				toolPath            : DYNARRAY[] of CHAR;
				displayName         : DYNARRAY[] of CHAR;
				shortcutKey         : CHAR;
				shortcutKeyModifier : INTEGER;
				resourceID          : INTEGER);
```

```python
def vs.ws2SetToolInfo(toolPath, displayName, shortcutKey, shortcutKeyModifier, resourceID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolPath|DYNARRAY[] of CHAR|   |
|displayName|DYNARRAY[] of CHAR|   |
|shortcutKey|CHAR|   |
|shortcutKeyModifier|INTEGER|   |
|resourceID|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
