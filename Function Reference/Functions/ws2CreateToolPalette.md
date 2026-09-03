# ws2CreateToolPalette

## Description
Workspace advanced APIs. Create a new tool palette if it doesn't exist.

```pascal
FUNCTION ws2CreateToolPalette(
				univName    : DYNARRAY[] of CHAR;
				displayName : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.ws2CreateToolPalette(univName, displayName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|univName|DYNARRAY[] of CHAR|   |
|displayName|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultOK := ws2CreateToolPalette(univName, displayName);
```
```python
import vs

# Workspace advanced APIs.
univName = 'Example'
displayName = 'Example'

ok = vs.ws2CreateToolPalette(univName, displayName)
if ok:
    vs.Message('ws2CreateToolPalette succeeded')
else:
    vs.Message('ws2CreateToolPalette failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Workspaces](../Categories/Workspaces.md)
