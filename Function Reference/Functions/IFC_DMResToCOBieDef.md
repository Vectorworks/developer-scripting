# IFC_DMResToCOBieDef

## Description
Resets the IFC Data Mapping Settings to Vectorworks COBie defaults.

```pascal
FUNCTION IFC_DMResToCOBieDef : BOOLEAN;
```

```python
def vs.IFC_DMResToCOBieDef():
    return BOOLEAN
```

## Examples
```pascal
resultOK := IFC_DMResToCOBieDef;
```
```python
import vs

# Resets the IFC Data Mapping Settings to Vectorworks COBie defaults.
ok = vs.IFC_DMResToCOBieDef()
if ok:
    vs.Message('IFC_DMResToCOBieDef succeeded')
else:
    vs.Message('IFC_DMResToCOBieDef failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
