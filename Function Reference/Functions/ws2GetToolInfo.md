# ws2GetToolInfo

## Description
Workspace advanced APIs. Return the tool information at the specified index of the parent tool at the specified path. See 'ws2GetToolsCnt'.

```pascal
FUNCTION ws2GetToolInfo(
				toolPath                   : DYNARRAY[] of CHAR;
				VAR outDisplayName         : DYNARRAY[] of CHAR;
				VAR outShortcutKey         : CHAR;
				VAR outShortcutKeyModifier : INTEGER;
				VAR outResourceID          : INTEGER): BOOLEAN;
```

```python
def vs.ws2GetToolInfo(toolPath):
    return (BOOLEAN, outDisplayName, outShortcutKey, outShortcutKeyModifier, outResourceID)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolPath|DYNARRAY[] of CHAR|   |
|outDisplayName|DYNARRAY[] of CHAR|   |
|outShortcutKey|CHAR|   |
|outShortcutKeyModifier|INTEGER|   |
|outResourceID|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
