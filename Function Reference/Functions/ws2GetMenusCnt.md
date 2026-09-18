# ws2GetMenusCnt

## Description
Workspace advanced APIs. Return the number of menu items at the speicfied path. Use '/' for path delimiter of universal menu names.

```pascal
FUNCTION ws2GetMenusCnt(menuPath : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.ws2GetMenusCnt(menuPath):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultN := ws2GetMenusCnt(menuPath);
```
```python
import vs

# Workspace advanced APIs.
menuPath = 'C:/Temp'

resultN = vs.ws2GetMenusCnt(menuPath)
vs.Message('ws2GetMenusCnt returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
