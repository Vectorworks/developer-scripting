# SetPaletteVisibility

## Description
Sets the visibility state of a palette.

```pascal
PROCEDURE SetPaletteVisibility(
				paletteName : STRING;
				vis         : BOOLEAN);
```

```python
def vs.SetPaletteVisibility(paletteName, vis):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|paletteName|STRING|Name of the palette|
|vis|BOOLEAN|True if the palette should be visible, false otherwise|

## Remarks
ptr 23-12-2019 - seems to work only on tool palets. Object Info, Attributes, ... don't react to the command.

## See Also
VS Functions:
[GetPaletteVisibility](GetPaletteVisibility.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Utility](../Categories/Utility.md)
