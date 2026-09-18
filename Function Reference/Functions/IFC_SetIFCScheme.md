# IFC_SetIFCScheme

## Description
Sets the active IFC version

```pascal
FUNCTION IFC_SetIFCScheme(scheme : INTEGER): BOOLEAN;
```

```python
def vs.IFC_SetIFCScheme(scheme):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|scheme|INTEGER|   |

## Examples
```pascal
resultOK := IFC_SetIFCScheme(1);
```
```python
import vs

# Sets the active IFC version.
scheme = 1

ok = vs.IFC_SetIFCScheme(scheme)
if ok:
    vs.Message('IFC_SetIFCScheme succeeded')
else:
    vs.Message('IFC_SetIFCScheme failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
