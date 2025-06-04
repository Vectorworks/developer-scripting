# ws2FindMenuIndex

## Description
Workspace advanced APIs. Return the indx of the specified universal name inside the provided menu path. Return -1 if not found. See 'ws2GetMenusCnt'.

```pascal
FUNCTION ws2FindMenuIndex(
				menuPath         : DYNARRAY[] of CHAR;
				findMenuUnivName : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.ws2FindMenuIndex(menuPath, findMenuUnivName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|DYNARRAY[] of CHAR|   |
|findMenuUnivName|DYNARRAY[] of CHAR|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
