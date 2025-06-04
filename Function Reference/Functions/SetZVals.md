# SetZVals

## Description
Procedure SetZVals sets the Z (layer base elevation) and delta Z (layer thickness) for the active layer.

```pascal
PROCEDURE SetZVals(
				zDistance      : REAL;
				deltaZDistance : REAL);
```

```python
def vs.SetZVals(zDistance, deltaZDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|zDistance|REAL|Layer base elevation (above document ground plane).|
|deltaZDistance|REAL|Layer thickness.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
baseElevation, thickness :REAL;
BEGIN
Layer('Test Layer');
baseElevation := 1;
thickness := 3;
SetZVals(baseElevation, thickness);
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from MiniCAD4.0

## Category
* [Layers](../Categories/Layers.md)
