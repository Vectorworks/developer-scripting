# IFC_CreateZSG

## Description
Creates Zone, System or Group based on the selector passed.

```pascal
FUNCTION IFC_CreateZSG(
				selector : INTEGER;
				ZSGName  : STRING): BOOLEAN;
```

```python
def vs.IFC_CreateZSG(selector, ZSGName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|ZSGName|STRING|   |

## Examples
```pascal
resultOK := IFC_CreateZSG(1, 'Example');
```
```python
import vs

# Creates Zone, System or Group based on the selector passed.
selector = 1
ZSGName = 'Example'

ok = vs.IFC_CreateZSG(selector, ZSGName)
if ok:
    vs.Message('IFC_CreateZSG succeeded')
else:
    vs.Message('IFC_CreateZSG failed')
```

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
