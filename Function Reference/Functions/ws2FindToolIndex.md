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

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
