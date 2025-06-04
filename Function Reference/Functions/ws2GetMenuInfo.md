# ws2GetMenuInfo

## Description
Workspace advanced APIs. Return the localized (if any) name, and shortkey combinations (if any) of the specified index inside the provided menu path. See 'ws2GetMenusCnt'.

```pascal
FUNCTION ws2GetMenuInfo(
				menuPath                   : DYNARRAY[] of CHAR;
				VAR outHasShortcutKey      : BOOLEAN;
				VAR outShortcutKey         : CHAR;
				VAR outShortcutKeyModifier : INTEGER): DYNARRAY[] of CHAR;
```

```python
def vs.ws2GetMenuInfo(menuPath):
    return (DYNARRAY[] of CHAR, outHasShortcutKey, outShortcutKey, outShortcutKeyModifier)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|DYNARRAY[] of CHAR|   |
|outHasShortcutKey|BOOLEAN|   |
|outShortcutKey|CHAR|   |
|outShortcutKeyModifier|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
