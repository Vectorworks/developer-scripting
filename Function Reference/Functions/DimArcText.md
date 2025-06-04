# DimArcText

## Description
Procedure DimArcText creates an angular dimension object from the last arc object that was drawn using VectorScript.

```pascal
PROCEDURE DimArcText;
```

```python
def vs.DimArcText():
    return None
```

## Remarks
Creates an angular dimension object from the last arc object that was drawn using VectorScript

## Examples
==== VectorScript ====
```pascal
Arc(0,0,2,2,45d,90d);
DimArcText;
{ creates a dimension from the new arc object }
```
==== Python ====
```python
vs.Arc(0,0,2,2,45,90)
vs.DimArcText()
```

## Version
Availability: from All Versions

## Category
* [Dimensions](../Categories/Dimensions.md)
