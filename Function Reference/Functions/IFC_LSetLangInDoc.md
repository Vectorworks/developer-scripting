# IFC_LSetLangInDoc

## Description
Sets the IFC Strings Localization in the Current Document.

```pascal
FUNCTION IFC_LSetLangInDoc(bIsIFCLocalized : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_LSetLangInDoc(bIsIFCLocalized):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|bIsIFCLocalized|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_LSetLangInDoc(TRUE);
```
```python
import vs

# Sets the IFC Strings Localization in the Current Document.
bIsIFCLocalized = True

ok = vs.IFC_LSetLangInDoc(bIsIFCLocalized)
if ok:
    vs.Message('IFC_LSetLangInDoc succeeded')
else:
    vs.Message('IFC_LSetLangInDoc failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
