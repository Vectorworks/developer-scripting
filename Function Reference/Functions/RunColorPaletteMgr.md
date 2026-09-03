# RunColorPaletteMgr

## Description
Runs the Color Palette Manager

```pascal
FUNCTION RunColorPaletteMgr : BOOLEAN;
```

```python
def vs.RunColorPaletteMgr():
    return BOOLEAN
```

## Examples
```pascal
resultOK := RunColorPaletteMgr;
```
```python
import vs

# Runs the Color Palette Manager.
ok = vs.RunColorPaletteMgr()
if ok:
    vs.Message('RunColorPaletteMgr succeeded')
else:
    vs.Message('RunColorPaletteMgr failed')
```

## Version
Availability: from Vectorworks 2013

## Category
* [Color](../Categories/Color.md)
