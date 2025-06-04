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

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
