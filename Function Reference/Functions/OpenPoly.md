# OpenPoly

## Description
Procedures OpenPoly set the polygon creation mode for polygon objects created in VectorScript to open. To turn this mode off, use Procedure ClosePoly; the two modes used in conjunction will act as a toggle for the feature.

```pascal
PROCEDURE OpenPoly;
```

```python
def vs.OpenPoly():
    return None
```

## Examples
==== VectorScript ====
```pascal
OpenPoly;
Poly(0,0,1,1,1,-1);
{creates a open 3 sided polygon}
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
