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

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
