# ws2GetToolAt

## Description
Workspace advanced APIs. Return the tool univ name at the specified index of the parent tool or tool set at the specified path. See 'ws2GetToolsCnt'.

```pascal
FUNCTION ws2GetToolAt(
				toolPath : DYNARRAY[] of CHAR;
				index    : INTEGER): DYNARRAY[] of CHAR;
```

```python
def vs.ws2GetToolAt(toolPath, index):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolPath|DYNARRAY[] of CHAR|   |
|index|INTEGER|   |

## Examples
```pascal
result := ws2GetToolAt(toolPath, 1);
```
```python
import vs

# Workspace advanced APIs.
toolPath = 'C:/Temp'
index = 1

text = vs.ws2GetToolAt(toolPath, index)
vs.Message('ws2GetToolAt returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
