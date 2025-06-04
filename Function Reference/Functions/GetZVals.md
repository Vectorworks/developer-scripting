# GetZVals

## Description
Procedure GetZVals returns the Z (layer base elevation) and delta Z (layer thickness) values for the active layer.

```pascal
PROCEDURE GetZVals(
				VAR zVal      : REAL;
				VAR deltaZVal : REAL);
```

```python
def vs.GetZVals():
    return (zVal, deltaZVal)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|zVal|REAL|Layer base elevation(above document ground plane).|
|deltaZVal|REAL|Layer thickness.|

## Remarks
Returns the Z and Delta Z values for the active layer.

[sd 8/14/98]

## Examples
#### VectorScript ####
```pascal
PROCEDURE GetLayerHeights(layerHandle :handle; var baseElev, thickness :REAL);
BEGIN
GetLayerElevation(layerHandle, baseElev, thickness);
baseElev  := baseElev  / (25.4 / GetPrefReal(152));
thickness := thickness / (25.4 / GetPrefReal(152));
END;
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD5.0

## Category
* [Layers](../Categories/Layers.md)
