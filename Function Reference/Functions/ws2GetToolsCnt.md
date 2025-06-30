# ws2GetToolsCnt

## Description
Workspace advanced APIs. Return the number of tools at the specified path composed of universal names &lt;tool palette&gt;/&lt;tool set&gt;. See [ws2GetMenusCnt](ws2GetMenusCnt.md).

```pascal
FUNCTION ws2GetToolsCnt(toolPath : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.ws2GetToolsCnt(toolPath):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolPath|DYNARRAY[] of CHAR|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
