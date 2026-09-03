# PenGrid

## Description
Procedure PenGrid sets the snap grid distance in the document.

```pascal
PROCEDURE PenGrid(gridDistance : REAL);
```

```python
def vs.PenGrid(gridDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gridDistance|REAL|Pen grid spacing.|

## Examples
```pascal
PenGrid (2*penGridD);
```
```python
import vs

# Procedure PenGrid sets the snap grid distance in the document.
gridDistance = 1.0

vs.PenGrid(gridDistance)
```

## Version
Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
