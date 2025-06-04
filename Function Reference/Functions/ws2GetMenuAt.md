# ws2GetMenuAt

## Description
Workspace advanced APIs. Return the universal name of the specified index inside the provided menu path See 'ws2GetMenusCnt'.

```pascal
FUNCTION ws2GetMenuAt(
				menuPath : DYNARRAY[] of CHAR;
				index    : INTEGER): DYNARRAY[] of CHAR;
```

```python
def vs.ws2GetMenuAt(menuPath, index):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuPath|DYNARRAY[] of CHAR|   |
|index|INTEGER|   |

## Remarks
Pat Stanford 4-20-21
The top level menu items do not seem to use the text version of the name as the "Universal Name"
but rather a UUID looking string. The positions are numbered starting at 0 (zero)

Use ws2GetMenuAt(ˈˈ, INDEX) where the first item is an empty string and INDEX is an integer specifying the menu item you are interested in to 
get the Universal Name of the View menu.

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
