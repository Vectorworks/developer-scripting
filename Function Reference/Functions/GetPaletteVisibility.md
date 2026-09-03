# GetPaletteVisibility

## Description
Gets the visibility state of a palette.

```pascal
FUNCTION GetPaletteVisibility(paletteName : STRING): BOOLEAN;
```

```python
def vs.GetPaletteVisibility(paletteName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|paletteName|STRING|Name of the palette|

## Remarks
oops, version obsolete is not correct.

oops, implemented version is not correct either.

## Examples
```pascal
resultOK := GetPaletteVisibility('Example');
```
```python
import vs

# Gets the visibility state of a palette.
paletteName = 'Example'

ok = vs.GetPaletteVisibility(paletteName)
if ok:
    vs.Message('GetPaletteVisibility succeeded')
else:
    vs.Message('GetPaletteVisibility failed')
```

## See Also
VS Functions:
[SetPaletteVisibility](SetPaletteVisibility.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Utility](../Categories/Utility.md)
