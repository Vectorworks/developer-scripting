# LightingInvImport

## Description
Imports Lighting inventory from data exchange file. Returns TRUE if items were imported.

```pascal
FUNCTION LightingInvImport : BOOLEAN;
```

```python
def vs.LightingInvImport():
    return BOOLEAN
```

## Examples
```pascal
resultOK := LightingInvImport;
```
```python
import vs

# Imports Lighting inventory from data exchange file.
ok = vs.LightingInvImport()
if ok:
    vs.Message('LightingInvImport succeeded')
else:
    vs.Message('LightingInvImport failed')
```

## Version
Availability: from Vectorworks 2015

## Category
* [Spotlight](../Categories/Spotlight.md)
