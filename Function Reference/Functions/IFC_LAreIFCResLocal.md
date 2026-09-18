# IFC_LAreIFCResLocal

## Description
Returns whether the Resources for the IFC Strings are Localized.

```pascal
FUNCTION IFC_LAreIFCResLocal(outbAreIFCResLocal : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_LAreIFCResLocal(outbAreIFCResLocal):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outbAreIFCResLocal|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_LAreIFCResLocal(TRUE);
```
```python
import vs

# Returns whether the Resources for the IFC Strings are Localized.
outbAreIFCResLocal = True

ok = vs.IFC_LAreIFCResLocal(outbAreIFCResLocal)
if ok:
    vs.Message('IFC_LAreIFCResLocal succeeded')
else:
    vs.Message('IFC_LAreIFCResLocal failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
