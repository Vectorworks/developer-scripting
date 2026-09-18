# ws2CreateTool

## Description
Workspace advanced APIs. Create a new tool.

```pascal
FUNCTION ws2CreateTool(
				toolPath   : DYNARRAY[] of CHAR;
				univName   : DYNARRAY[] of CHAR;
				resourceID : INTEGER): BOOLEAN;
```

```python
def vs.ws2CreateTool(toolPath, univName, resourceID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolPath|DYNARRAY[] of CHAR|   |
|univName|DYNARRAY[] of CHAR|   |
|resourceID|INTEGER|   |

## Remarks
resourceID:

SDK Tool = 1

VectorScript Tool = 2

VectorScript Object = 3

SDK Parametric = 4

## Examples
```pascal
resultOK := ws2CreateTool(toolPath, univName, 1);
```
```python
import vs

# Workspace advanced APIs.
toolPath = 'C:/Temp'
univName = 'Example'
resourceID = 1

ok = vs.ws2CreateTool(toolPath, univName, resourceID)
if ok:
    vs.Message('ws2CreateTool succeeded')
else:
    vs.Message('ws2CreateTool failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
