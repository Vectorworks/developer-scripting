# IFC_LSetLangInVW

## Description
Sets the IFC Strings Localization in the Vectorworks.

```pascal
FUNCTION IFC_LSetLangInVW(bIsIFCLocalized : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_LSetLangInVW(bIsIFCLocalized):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|bIsIFCLocalized|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_LSetLangInVW(TRUE);
```
```python
import vs

# Sets the IFC Strings Localization in the Vectorworks.
bIsIFCLocalized = True

ok = vs.IFC_LSetLangInVW(bIsIFCLocalized)
if ok:
    vs.Message('IFC_LSetLangInVW succeeded')
else:
    vs.Message('IFC_LSetLangInVW failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
