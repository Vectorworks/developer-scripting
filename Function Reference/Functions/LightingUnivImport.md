# LightingUnivImport

## Description
Imports Lighting universe settings from data exchange file. Returns TRUE if any universes were changed.

```pascal
FUNCTION LightingUnivImport : BOOLEAN;
```

```python
def vs.LightingUnivImport():
    return BOOLEAN
```

## Examples
```pascal
resultOK := LightingUnivImport;
```
```python
import vs

# Imports Lighting universe settings from data exchange file.
ok = vs.LightingUnivImport()
if ok:
    vs.Message('LightingUnivImport succeeded')
else:
    vs.Message('LightingUnivImport failed')
```

## Version
Availability: from Vectorworks 2015

## Category
* [Spotlight](../Categories/Spotlight.md)
