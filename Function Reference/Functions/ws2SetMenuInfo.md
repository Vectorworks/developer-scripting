# ws2SetMenuInfo

## Description
Workspace advanced APIs. Set the localized (if any) name, and shortkey combinations (if any) of the specified index inside the provided menu path. See 'ws2GetMenusCnt'.

```pascal
PROCEDURE ws2SetMenuInfo(
				menuPath            : DYNARRAY[] of CHAR;
				displayName         : DYNARRAY[] of CHAR;
				hasShortcutKey      : BOOLEAN;
				shortcutKey         : CHAR;
				shortcutKeyModifier : INTEGER);
```

```python
def vs.ws2SetMenuInfo(menuPath, displayName, hasShortcutKey, shortcutKey, shortcutKeyModifier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|DYNARRAY[] of CHAR|   |
|displayName|DYNARRAY[] of CHAR|   |
|hasShortcutKey|BOOLEAN|   |
|shortcutKey|CHAR|   |
|shortcutKeyModifier|INTEGER|   |

## Examples
```pascal
ws2SetMenuInfo(menuPath, displayName, TRUE, shortcutKey, 1);
```
```python
import vs

# Workspace advanced APIs.
menuPath = 'C:/Temp'
displayName = 'Example'
hasShortcutKey = True
shortcutKey = 'Example'
shortcutKeyModifier = 1

vs.ws2SetMenuInfo(menuPath, displayName, hasShortcutKey, shortcutKey, shortcutKeyModifier)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
