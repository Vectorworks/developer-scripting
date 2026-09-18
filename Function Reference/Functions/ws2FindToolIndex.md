# ws2FindToolIndex

## Description
Workspace advanced APIs. Return the named tool index at the specified path. See 'ws2GetToolsCnt'.

```pascal
FUNCTION ws2FindToolIndex(
				toolPath     : DYNARRAY[] of CHAR;
				findUnivName : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.ws2FindToolIndex(toolPath, findUnivName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolPath|DYNARRAY[] of CHAR|   |
|findUnivName|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultN := ws2FindToolIndex(toolPath, findUnivName);
```
```python
import vs

# Workspace advanced APIs.
toolPath = 'C:/Temp'
findUnivName = 'Example'

index = vs.ws2FindToolIndex(toolPath, findUnivName)
vs.Message('ws2FindToolIndex returned: ' + str(index))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
