# IFC_LGetLangFromDoc

## Description
Returns whether the IFC Strings are Localized.

```pascal
FUNCTION IFC_LGetLangFromDoc(outbIsIFCLocalized : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_LGetLangFromDoc(outbIsIFCLocalized):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outbIsIFCLocalized|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_LGetLangFromDoc(TRUE);
```
```python
import vs

# Returns whether the IFC Strings are Localized.
outbIsIFCLocalized = True

ok = vs.IFC_LGetLangFromDoc(outbIsIFCLocalized)
if ok:
    vs.Message('IFC_LGetLangFromDoc succeeded')
else:
    vs.Message('IFC_LGetLangFromDoc failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
