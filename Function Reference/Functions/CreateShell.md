# CreateShell

## Description
Creates a shelled solid from a NURBS surface.

```pascal
FUNCTION CreateShell(
				surface   : HANDLE;
				thickness : REAL): Handle;
```

```python
def vs.CreateShell(surface, thickness):
    return Handle
```

## Parameters
|Name|Type|Description|
|---|---|---|
|surface|HANDLE|   |
|thickness|REAL|   |

## Examples
```pascal
resultH := CreateShell(surface, 1.0);
```
```python
import vs

# Creates a shelled solid from a NURBS surface.
surface = vs.FSActLayer()  # handle to the first selected object on the active layer
thickness = 0.1

objHandle = vs.CreateShell(surface, thickness)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
