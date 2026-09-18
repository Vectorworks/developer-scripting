# ws2AddMenuItem

## Description
Workspace advanced APIs. Adds a new menu item by universal name before the specified index (-1 for the end) inside the provided menu path. See 'ws2GetMenusCnt'.

```pascal
FUNCTION ws2AddMenuItem(
				menuPath        : DYNARRAY[] of CHAR;
				newMenuUnivName : DYNARRAY[] of CHAR;
				beforeIndex     : INTEGER): BOOLEAN;
```

```python
def vs.ws2AddMenuItem(menuPath, newMenuUnivName, beforeIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|DYNARRAY[] of CHAR|   |
|newMenuUnivName|DYNARRAY[] of CHAR|   |
|beforeIndex|INTEGER|   |

## Examples
```pascal
resultOK := ws2AddMenuItem(menuPath, newMenuUnivName, 1);
```
```python
import vs

# Workspace advanced APIs.
menuPath = 'C:/Temp'
newMenuUnivName = 'Example'
beforeIndex = 1

ok = vs.ws2AddMenuItem(menuPath, newMenuUnivName, beforeIndex)
if ok:
    vs.Message('ws2AddMenuItem succeeded')
else:
    vs.Message('ws2AddMenuItem failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
